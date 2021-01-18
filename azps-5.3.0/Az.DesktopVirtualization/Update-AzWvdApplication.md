---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 87932f3f703ba1ffe8ae7e367d44445166728032
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499249"
---
# <span data-ttu-id="df9b4-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="df9b4-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="df9b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df9b4-102">SYNOPSIS</span></span>
<span data-ttu-id="df9b4-103">Aktualizowanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="df9b4-103">Update an application.</span></span>

## <span data-ttu-id="df9b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df9b4-104">SYNTAX</span></span>

### <span data-ttu-id="df9b4-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="df9b4-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="df9b4-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="df9b4-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="df9b4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="df9b4-107">DESCRIPTION</span></span>
<span data-ttu-id="df9b4-108">Aktualizowanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="df9b4-108">Update an application.</span></span>

## <span data-ttu-id="df9b4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df9b4-109">EXAMPLES</span></span>

### <span data-ttu-id="df9b4-110">Przykład 1: aktualizowanie aplikacji klasycznej Windows Virtual</span><span class="sxs-lookup"><span data-stu-id="df9b4-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> Update-AzWvdApplication -ResourceGroupName ResourceGroupName `
                             -GroupName ApplicationGroupName `
                             -Name ApplicationName `
                             -FilePath 'C:\windows\system32\mspaint.exe' `
                             -FriendlyName 'Friendly name' `
                             -Description 'Description' `
                             -IconIndex 0 `
                             -IconPath 'C:\windows\system32\mspaint.exe' `
                             -CommandLineSetting 'Allow' `
                             -ShowInPortal:$true

Name                                 Type
----                                 ----
ApplicationGroupName/ApplicationName Microsoft.DesktopVirtualization/applicationgroups/applications
```

<span data-ttu-id="df9b4-111">To polecenie aktualizuje aplikację klasyczną systemu Windows w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="df9b4-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="df9b4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df9b4-112">PARAMETERS</span></span>

### <span data-ttu-id="df9b4-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="df9b4-113">-ApplicationType</span></span>
<span data-ttu-id="df9b4-114">Typ zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="df9b4-114">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="df9b4-115">-CommandLineArgument</span></span>
<span data-ttu-id="df9b4-116">Argumenty wiersza polecenia dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="df9b4-116">Command Line Arguments for Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="df9b4-117">-CommandLineSetting</span></span>
<span data-ttu-id="df9b4-118">Określa, czy ta opublikowana aplikacja może być uruchamiana z argumentami wiersza polecenia dostarczonymi przez klienta, argumenty wiersza polecenia określone w czasie publikowania lub bez argumentów wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="df9b4-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9b4-119">-DefaultProfile</span></span>
<span data-ttu-id="df9b4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df9b4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="df9b4-121">-Description</span></span>
<span data-ttu-id="df9b4-122">Opis aplikacji.</span><span class="sxs-lookup"><span data-stu-id="df9b4-122">Description of Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="df9b4-123">-FilePath</span></span>
<span data-ttu-id="df9b4-124">Określa ścieżkę pliku wykonywalnego aplikacji.</span><span class="sxs-lookup"><span data-stu-id="df9b4-124">Specifies a path for the executable file for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="df9b4-125">-FriendlyName</span></span>
<span data-ttu-id="df9b4-126">Przyjazna nazwa aplikacji.</span><span class="sxs-lookup"><span data-stu-id="df9b4-126">Friendly name of Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="df9b4-127">-GroupName</span></span>
<span data-ttu-id="df9b4-128">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="df9b4-128">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="df9b4-129">-IconIndex</span></span>
<span data-ttu-id="df9b4-130">Indeks ikony.</span><span class="sxs-lookup"><span data-stu-id="df9b4-130">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="df9b4-131">-IconPath</span></span>
<span data-ttu-id="df9b4-132">Ścieżka do ikony.</span><span class="sxs-lookup"><span data-stu-id="df9b4-132">Path to icon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="df9b4-133">-InputObject</span></span>
<span data-ttu-id="df9b4-134">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="df9b4-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="df9b4-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="df9b4-136">Określa identyfikator aplikacji pakietu dla aplikacji MSIX</span><span class="sxs-lookup"><span data-stu-id="df9b4-136">Specifies the package application Id for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="df9b4-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="df9b4-138">Określa nazwę rodziny pakietów dla aplikacji MSIX</span><span class="sxs-lookup"><span data-stu-id="df9b4-138">Specifies the package family name for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="df9b4-139">-Name</span></span>
<span data-ttu-id="df9b4-140">Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="df9b4-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df9b4-141">-ResourceGroupName</span></span>
<span data-ttu-id="df9b4-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df9b4-142">The name of the resource group.</span></span>
<span data-ttu-id="df9b4-143">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="df9b4-143">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="df9b4-144">-ShowInPortal</span></span>
<span data-ttu-id="df9b4-145">Określa, czy Program RemoteApp ma być pokazywany na serwerze programu dostęp w sieci Web do usług pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="df9b4-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-146">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="df9b4-146">-SubscriptionId</span></span>
<span data-ttu-id="df9b4-147">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="df9b4-147">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="df9b4-148">-Tag</span></span>
<span data-ttu-id="df9b4-149">Tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="df9b4-149">tags to be updated</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df9b4-150">-Confirm</span></span>
<span data-ttu-id="df9b4-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df9b4-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df9b4-152">-WhatIf</span></span>
<span data-ttu-id="df9b4-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df9b4-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df9b4-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="df9b4-154">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df9b4-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9b4-155">CommonParameters</span></span>
<span data-ttu-id="df9b4-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df9b4-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9b4-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df9b4-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9b4-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df9b4-158">INPUTS</span></span>

### <span data-ttu-id="df9b4-159">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="df9b4-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="df9b4-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df9b4-160">OUTPUTS</span></span>

### <span data-ttu-id="df9b4-161">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201102Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="df9b4-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="df9b4-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df9b4-162">NOTES</span></span>

<span data-ttu-id="df9b4-163">PISUJE</span><span class="sxs-lookup"><span data-stu-id="df9b4-163">ALIASES</span></span>

<span data-ttu-id="df9b4-164">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df9b4-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="df9b4-165">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="df9b4-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="df9b4-166">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="df9b4-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="df9b4-167">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="df9b4-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="df9b4-168">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="df9b4-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="df9b4-169">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="df9b4-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="df9b4-170">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="df9b4-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="df9b4-171">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="df9b4-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="df9b4-172">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="df9b4-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="df9b4-173">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="df9b4-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="df9b4-174">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="df9b4-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="df9b4-175">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="df9b4-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="df9b4-176">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="df9b4-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="df9b4-177">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="df9b4-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="df9b4-178">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="df9b4-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="df9b4-179">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="df9b4-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="df9b4-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df9b4-180">RELATED LINKS</span></span>

