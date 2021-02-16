---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 87932f3f703ba1ffe8ae7e367d44445166728032
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243818"
---
# <span data-ttu-id="4da64-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="4da64-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="4da64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4da64-102">SYNOPSIS</span></span>
<span data-ttu-id="4da64-103">Zaktualizuj aplikację.</span><span class="sxs-lookup"><span data-stu-id="4da64-103">Update an application.</span></span>

## <span data-ttu-id="4da64-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4da64-104">SYNTAX</span></span>

### <span data-ttu-id="4da64-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="4da64-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4da64-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4da64-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity>
 [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4da64-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="4da64-107">DESCRIPTION</span></span>
<span data-ttu-id="4da64-108">Zaktualizuj aplikację.</span><span class="sxs-lookup"><span data-stu-id="4da64-108">Update an application.</span></span>

## <span data-ttu-id="4da64-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4da64-109">EXAMPLES</span></span>

### <span data-ttu-id="4da64-110">Przykład 1. Aktualizowanie aplikacji pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="4da64-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="4da64-111">To polecenie aktualizuje aplikację pulpitu wirtualnego systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4da64-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="4da64-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4da64-112">PARAMETERS</span></span>

### <span data-ttu-id="4da64-113">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="4da64-113">-ApplicationType</span></span>
<span data-ttu-id="4da64-114">Typ zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4da64-114">Resource Type of Application.</span></span>

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

### <span data-ttu-id="4da64-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="4da64-115">-CommandLineArgument</span></span>
<span data-ttu-id="4da64-116">Argumenty wiersza polecenia dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4da64-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="4da64-117">- CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="4da64-117">-CommandLineSetting</span></span>
<span data-ttu-id="4da64-118">Określa, czy tę opublikowaną aplikację można uruchomić z argumentami wiersza polecenia dostarczonymi przez klienta, argumentami wiersza polecenia określonymi w czasie publikowania, czy też w ogóle nie ma argumentów wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="4da64-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="4da64-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4da64-119">-DefaultProfile</span></span>
<span data-ttu-id="4da64-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4da64-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4da64-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="4da64-121">-Description</span></span>
<span data-ttu-id="4da64-122">Opis aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4da64-122">Description of Application.</span></span>

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

### <span data-ttu-id="4da64-123">- FilePath</span><span class="sxs-lookup"><span data-stu-id="4da64-123">-FilePath</span></span>
<span data-ttu-id="4da64-124">Określa ścieżkę pliku wykonywalnego dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4da64-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="4da64-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4da64-125">-FriendlyName</span></span>
<span data-ttu-id="4da64-126">Przyjazna nazwa aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4da64-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="4da64-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="4da64-127">-GroupName</span></span>
<span data-ttu-id="4da64-128">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4da64-128">The name of the application group</span></span>

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

### <span data-ttu-id="4da64-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="4da64-129">-IconIndex</span></span>
<span data-ttu-id="4da64-130">Indeks ikony.</span><span class="sxs-lookup"><span data-stu-id="4da64-130">Index of the icon.</span></span>

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

### <span data-ttu-id="4da64-131">— IconPath</span><span class="sxs-lookup"><span data-stu-id="4da64-131">-IconPath</span></span>
<span data-ttu-id="4da64-132">Ikona Ścieżka do.</span><span class="sxs-lookup"><span data-stu-id="4da64-132">Path to icon.</span></span>

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

### <span data-ttu-id="4da64-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4da64-133">-InputObject</span></span>
<span data-ttu-id="4da64-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="4da64-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4da64-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="4da64-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="4da64-136">Określa identyfikator aplikacji pakietu dla aplikacji MSIX.</span><span class="sxs-lookup"><span data-stu-id="4da64-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="4da64-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="4da64-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="4da64-138">Określa nazwę rodziny pakietów dla aplikacji MSIX.</span><span class="sxs-lookup"><span data-stu-id="4da64-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="4da64-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4da64-139">-Name</span></span>
<span data-ttu-id="4da64-140">Nazwa aplikacji w obrębie określonej grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4da64-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="4da64-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4da64-141">-ResourceGroupName</span></span>
<span data-ttu-id="4da64-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4da64-142">The name of the resource group.</span></span>
<span data-ttu-id="4da64-143">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="4da64-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="4da64-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="4da64-144">-ShowInPortal</span></span>
<span data-ttu-id="4da64-145">Określa, czy program RemoteApp ma być pokazywany na serwerze RD Web Access.</span><span class="sxs-lookup"><span data-stu-id="4da64-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="4da64-146">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4da64-146">-SubscriptionId</span></span>
<span data-ttu-id="4da64-147">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4da64-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="4da64-148">— Tag</span><span class="sxs-lookup"><span data-stu-id="4da64-148">-Tag</span></span>
<span data-ttu-id="4da64-149">tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="4da64-149">tags to be updated</span></span>

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

### <span data-ttu-id="4da64-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4da64-150">-Confirm</span></span>
<span data-ttu-id="4da64-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4da64-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4da64-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4da64-152">-WhatIf</span></span>
<span data-ttu-id="4da64-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4da64-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4da64-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4da64-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4da64-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4da64-155">CommonParameters</span></span>
<span data-ttu-id="4da64-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4da64-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4da64-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4da64-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4da64-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4da64-158">INPUTS</span></span>

### <span data-ttu-id="4da64-159">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4da64-159">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4da64-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4da64-160">OUTPUTS</span></span>

### <span data-ttu-id="4da64-161">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="4da64-161">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="4da64-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4da64-162">NOTES</span></span>

<span data-ttu-id="4da64-163">ALIASY</span><span class="sxs-lookup"><span data-stu-id="4da64-163">ALIASES</span></span>

<span data-ttu-id="4da64-164">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="4da64-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4da64-165">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4da64-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4da64-166">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4da64-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4da64-167">INPUTOBJECT: <IDesktopVirtualizationIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="4da64-167">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4da64-168">`[ApplicationGroupName <String>]`: nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4da64-168">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4da64-169">`[ApplicationName <String>]`: nazwa aplikacji w obrębie określonej grupy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4da64-169">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4da64-170">`[DesktopName <String>]`: nazwa pulpitu w obrębie określonej grupy pulpitów;</span><span class="sxs-lookup"><span data-stu-id="4da64-170">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4da64-171">`[HostPoolName <String>]`: nazwa puli hostów w obrębie określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4da64-171">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4da64-172">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4da64-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4da64-173">`[MsixPackageFullName <String>]`: Pełna nazwa pakietu MSIX dla określonej wersji w ramach określonego buforu hosta</span><span class="sxs-lookup"><span data-stu-id="4da64-173">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4da64-174">`[ResourceGroupName <String>]`: nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4da64-174">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4da64-175">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="4da64-175">The name is case insensitive.</span></span>
  - <span data-ttu-id="4da64-176">`[SessionHostName <String>]`: nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="4da64-176">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4da64-177">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4da64-177">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4da64-178">`[UserSessionId <String>]`: nazwa sesji użytkownika na określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="4da64-178">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4da64-179">`[WorkspaceName <String>]`: nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="4da64-179">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4da64-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4da64-180">RELATED LINKS</span></span>

