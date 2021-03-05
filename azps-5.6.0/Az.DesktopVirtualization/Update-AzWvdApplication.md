---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8770b9e3b07b677f0f4bd4f59a6c38928421523e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001617"
---
# <span data-ttu-id="cd299-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="cd299-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="cd299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd299-102">SYNOPSIS</span></span>
<span data-ttu-id="cd299-103">Zaktualizuj aplikację.</span><span class="sxs-lookup"><span data-stu-id="cd299-103">Update an application.</span></span>

## <span data-ttu-id="cd299-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd299-104">SYNTAX</span></span>

### <span data-ttu-id="cd299-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="cd299-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd299-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="cd299-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd299-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd299-107">DESCRIPTION</span></span>
<span data-ttu-id="cd299-108">Zaktualizuj aplikację.</span><span class="sxs-lookup"><span data-stu-id="cd299-108">Update an application.</span></span>

## <span data-ttu-id="cd299-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd299-109">EXAMPLES</span></span>

### <span data-ttu-id="cd299-110">Przykład 1. Aktualizowanie aplikacji pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="cd299-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="cd299-111">To polecenie aktualizuje aplikację pulpitu wirtualnego systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd299-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="cd299-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd299-112">PARAMETERS</span></span>

### <span data-ttu-id="cd299-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="cd299-113">-ApplicationType</span></span>
<span data-ttu-id="cd299-114">Typ zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd299-114">Resource Type of Application.</span></span>

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

### <span data-ttu-id="cd299-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="cd299-115">-CommandLineArgument</span></span>
<span data-ttu-id="cd299-116">Argumenty wiersza polecenia dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd299-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="cd299-117">- CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="cd299-117">-CommandLineSetting</span></span>
<span data-ttu-id="cd299-118">Określa, czy tę opublikowaną aplikację można uruchomić z argumentami wiersza polecenia dostarczonymi przez klienta, argumentami wiersza polecenia określonymi w czasie publikowania, czy też w ogóle nie ma argumentów wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="cd299-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="cd299-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd299-119">-DefaultProfile</span></span>
<span data-ttu-id="cd299-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd299-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd299-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="cd299-121">-Description</span></span>
<span data-ttu-id="cd299-122">Opis aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd299-122">Description of Application.</span></span>

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

### <span data-ttu-id="cd299-123">- FilePath</span><span class="sxs-lookup"><span data-stu-id="cd299-123">-FilePath</span></span>
<span data-ttu-id="cd299-124">Określa ścieżkę pliku wykonywalnego dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd299-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="cd299-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="cd299-125">-FriendlyName</span></span>
<span data-ttu-id="cd299-126">Przyjazna nazwa aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd299-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="cd299-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="cd299-127">-GroupName</span></span>
<span data-ttu-id="cd299-128">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="cd299-128">The name of the application group</span></span>

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

### <span data-ttu-id="cd299-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="cd299-129">-IconIndex</span></span>
<span data-ttu-id="cd299-130">Indeks ikony.</span><span class="sxs-lookup"><span data-stu-id="cd299-130">Index of the icon.</span></span>

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

### <span data-ttu-id="cd299-131">— IconPath</span><span class="sxs-lookup"><span data-stu-id="cd299-131">-IconPath</span></span>
<span data-ttu-id="cd299-132">Ikona Ścieżka do.</span><span class="sxs-lookup"><span data-stu-id="cd299-132">Path to icon.</span></span>

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

### <span data-ttu-id="cd299-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd299-133">-InputObject</span></span>
<span data-ttu-id="cd299-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="cd299-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cd299-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="cd299-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="cd299-136">Określa identyfikator aplikacji pakietu dla aplikacji MSIX.</span><span class="sxs-lookup"><span data-stu-id="cd299-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="cd299-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="cd299-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="cd299-138">Określa nazwę rodziny pakietów dla aplikacji MSIX.</span><span class="sxs-lookup"><span data-stu-id="cd299-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="cd299-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cd299-139">-Name</span></span>
<span data-ttu-id="cd299-140">Nazwa aplikacji w obrębie określonej grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="cd299-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="cd299-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd299-141">-ResourceGroupName</span></span>
<span data-ttu-id="cd299-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd299-142">The name of the resource group.</span></span>
<span data-ttu-id="cd299-143">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="cd299-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="cd299-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="cd299-144">-ShowInPortal</span></span>
<span data-ttu-id="cd299-145">Określa, czy program RemoteApp ma być pokazywany na serwerze RD Web Access.</span><span class="sxs-lookup"><span data-stu-id="cd299-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="cd299-146">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd299-146">-SubscriptionId</span></span>
<span data-ttu-id="cd299-147">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="cd299-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="cd299-148">— Tag</span><span class="sxs-lookup"><span data-stu-id="cd299-148">-Tag</span></span>
<span data-ttu-id="cd299-149">tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="cd299-149">tags to be updated</span></span>

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

### <span data-ttu-id="cd299-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd299-150">-Confirm</span></span>
<span data-ttu-id="cd299-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cd299-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd299-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd299-152">-WhatIf</span></span>
<span data-ttu-id="cd299-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd299-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd299-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cd299-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd299-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd299-155">CommonParameters</span></span>
<span data-ttu-id="cd299-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd299-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd299-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd299-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd299-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd299-158">INPUTS</span></span>

### <span data-ttu-id="cd299-159">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="cd299-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="cd299-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd299-160">OUTPUTS</span></span>

### <span data-ttu-id="cd299-161">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="cd299-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="cd299-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd299-162">NOTES</span></span>

<span data-ttu-id="cd299-163">ALIASY</span><span class="sxs-lookup"><span data-stu-id="cd299-163">ALIASES</span></span>

<span data-ttu-id="cd299-164">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd299-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cd299-165">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cd299-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd299-166">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd299-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cd299-167">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="cd299-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd299-168">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="cd299-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="cd299-169">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cd299-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="cd299-170">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="cd299-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="cd299-171">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd299-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="cd299-172">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cd299-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd299-173">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="cd299-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="cd299-174">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd299-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cd299-175">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="cd299-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="cd299-176">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="cd299-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="cd299-177">`[SubscriptionId <String>]`: identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="cd299-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cd299-178">`[UserSessionId <String>]`: nazwa sesji użytkownika w obrębie określonego hosta sesji.</span><span class="sxs-lookup"><span data-stu-id="cd299-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="cd299-179">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="cd299-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="cd299-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd299-180">RELATED LINKS</span></span>

