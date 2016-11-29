---
title: Preparing to Use TraceView
description: Preparing to Use TraceView
ms.assetid: 724e3c8a-7760-4e53-8d44-1927e5ad1efd
keywords: ["TraceView WDK , preparing to use", "files WDK TraceView"]
---

# Preparing to Use TraceView


## <span id="ddk_preparing_to_use_traceview_tools"></span><span id="DDK_PREPARING_TO_USE_TRACEVIEW_TOOLS"></span>


Before you use TraceView, you need to gather information about event tracing and about the [trace provider](trace-provider.md) that you are tracing. This topic describes these prerequisites.

**Note**   If you are running TraceView on versions of the Windows operating system earlier than Windows Vista , you must copy the Dbghelp.dll file to the same subdirectory as the TraceView executable file, TraceView.exe. By default, TraceView.exe is located in the tools\\tracing\\*&lt;Platform&gt;* subdirectory of the Windows Driver Kit (WDK), where *&lt;Platform&gt;* is either i386, amd64, or ia64. The Dbghelp.dll is installed, by default, in the \\bin\\x86 subdirectory.

 

### <span id="understand_event_tracing"></span><span id="UNDERSTAND_EVENT_TRACING"></span>Understand Event Tracing

Before you use TraceView, you should be familiar with *event tracing*. For more information, see [WPP Software Tracing](wpp-software-tracing.md) and the "[Event Tracing](http://go.microsoft.com/fwlink/p/?linkid=60384)" topic in the Microsoft Windows SDK.

Also, examine Tracedrv (Tracedrv.c), a sample driver instrumented with WPP software tracing. The [Tracedrv](http://go.microsoft.com/fwlink/p/?LinkId=617726) sample is available in the [Windows driver samples](http://go.microsoft.com/fwlink/p/?LinkId=616507 ) repository on GitHub. Build the Tracedrv driver and its engine, Tracectl (Tracectl.c), and then use the driver and engine to experiment with TraceView.

### <span id="know_the_trace_provider"></span><span id="KNOW_THE_TRACE_PROVIDER"></span>Know the Trace Provider

You should be familiar with the [trace provider](trace-provider.md) that you are tracing, and the types of trace messages that it generates.

TraceView displays trace event and trace messages in a human-readable format, but it does not interpret them or provide any information or context for the messages. To understand the messages and what they indicate about the provider, you must be very familiar with the operation of the provider.

### <span id="find_provider_files"></span><span id="FIND_PROVIDER_FILES"></span>Find Provider Files

To view the trace messages from a trace provider, you will need to provide one of the following locations to TraceView:

-   The location of the [PDB symbol file](pdb-symbol-files.md) for the provider

-   - OR -

-   The location of the [control GUID (.ctl) file](control-guid-file.md) for the provider and the location of the [trace message format (.tmf) file](trace-message-format-file.md) for its trace messages

The [NT Kernel Logger Trace Session](nt-kernel-logger-trace-session.md) uses the system.tmf file that is included in the WDK (\\tools\\tracing\\i386\).

These files, and their use in TraceView, are described in [Creating an NT Kernel Logger Trace Session](creating-an-nt-kernel-logger-trace-session.md). You will use this information when you create a trace session.

 

 

[Send comments about this topic to Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20[devtest\devtest]:%20Preparing%20to%20Use%20TraceView%20%20RELEASE:%20%2811/17/2016%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Send comments about this topic to Microsoft")



