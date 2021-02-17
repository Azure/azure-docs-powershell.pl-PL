---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 88c56275bc2687d9693411159551684a9c76f943
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196442"
---
# <span data-ttu-id="62641-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="62641-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="62641-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62641-102">SYNOPSIS</span></span>
<span data-ttu-id="62641-103">Utwórz lub zaktualizuj aplikację.</span><span class="sxs-lookup"><span data-stu-id="62641-103">Create or update an application.</span></span>

## <span data-ttu-id="62641-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62641-104">SYNTAX</span></span>

### <span data-ttu-id="62641-105">CreateExpanded (Default)</span><span class="sxs-lookup"><span data-stu-id="62641-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="62641-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="62641-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="62641-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="62641-107">DESCRIPTION</span></span>
<span data-ttu-id="62641-108">Utwórz lub zaktualizuj aplikację.</span><span class="sxs-lookup"><span data-stu-id="62641-108">Create or update an application.</span></span>

## <span data-ttu-id="62641-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62641-109">EXAMPLES</span></span>

### <span data-ttu-id="62641-110">Przykład 1. Tworzenie aplikacji pulpitu wirtualnego systemu Windows</span><span class="sxs-lookup"><span data-stu-id="62641-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
```powershell
PS C:\> New-AzWvdApplication -ResourceGroupName ResourceGroupName `
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

<span data-ttu-id="62641-111">To polecenie tworzy aplikację pulpitu wirtualnego systemu Windows w grupie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62641-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="62641-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62641-112">PARAMETERS</span></span>

### <span data-ttu-id="62641-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="62641-113">-AppAlias</span></span>
<span data-ttu-id="62641-114">Pozycja menu Alias aplikacji z menu Start</span><span class="sxs-lookup"><span data-stu-id="62641-114">App Alias from start menu item</span></span>

```yaml
Type: System.String
Parameter Sets: AppAlias
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="62641-115">-ApplicationType</span></span>
<span data-ttu-id="62641-116">Typ zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62641-116">Resource Type of Application.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.RemoteApplicationType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="62641-117">-CommandLineArgument</span></span>
<span data-ttu-id="62641-118">Argumenty wiersza polecenia dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62641-118">Command Line Arguments for Application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-119">- CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="62641-119">-CommandLineSetting</span></span>
<span data-ttu-id="62641-120">Określa, czy tę opublikowaną aplikację można uruchomić z argumentami wiersza polecenia dostarczonymi przez klienta, argumentami wiersza polecenia określonymi w czasie publikowania, czy też w ogóle nie ma argumentów wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="62641-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Support.CommandLineSetting
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62641-121">-DefaultProfile</span></span>
<span data-ttu-id="62641-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62641-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62641-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="62641-123">-Description</span></span>
<span data-ttu-id="62641-124">Opis aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62641-124">Description of Application.</span></span>

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

### <span data-ttu-id="62641-125">- FilePath</span><span class="sxs-lookup"><span data-stu-id="62641-125">-FilePath</span></span>
<span data-ttu-id="62641-126">Określa ścieżkę pliku wykonywalnego dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62641-126">Specifies a path for the executable file for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="62641-127">-FriendlyName</span></span>
<span data-ttu-id="62641-128">Przyjazna nazwa aplikacji.</span><span class="sxs-lookup"><span data-stu-id="62641-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="62641-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="62641-129">-GroupName</span></span>
<span data-ttu-id="62641-130">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="62641-130">The name of the application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="62641-131">-IconIndex</span></span>
<span data-ttu-id="62641-132">Indeks ikony.</span><span class="sxs-lookup"><span data-stu-id="62641-132">Index of the icon.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-133">— IconPath</span><span class="sxs-lookup"><span data-stu-id="62641-133">-IconPath</span></span>
<span data-ttu-id="62641-134">Ikona Ścieżka do.</span><span class="sxs-lookup"><span data-stu-id="62641-134">Path to icon.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="62641-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="62641-136">Określa identyfikator aplikacji pakietu dla aplikacji MSIX.</span><span class="sxs-lookup"><span data-stu-id="62641-136">Specifies the package application Id for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="62641-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="62641-138">Określa nazwę rodziny pakietów dla aplikacji MSIX.</span><span class="sxs-lookup"><span data-stu-id="62641-138">Specifies the package family name for MSIX applications</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="62641-139">-Name</span></span>
<span data-ttu-id="62641-140">Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="62641-140">The name of the application within the specified application group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62641-141">-ResourceGroupName</span></span>
<span data-ttu-id="62641-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="62641-142">The name of the resource group.</span></span>
<span data-ttu-id="62641-143">W nazwie nie jest uwzględniania liter.</span><span class="sxs-lookup"><span data-stu-id="62641-143">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="62641-144">-ShowInPortal</span></span>
<span data-ttu-id="62641-145">Określa, czy program RemoteApp ma być pokazywany na serwerze RD Web Access.</span><span class="sxs-lookup"><span data-stu-id="62641-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="62641-146">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="62641-146">-SubscriptionId</span></span>
<span data-ttu-id="62641-147">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="62641-147">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62641-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62641-148">-Confirm</span></span>
<span data-ttu-id="62641-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62641-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62641-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62641-150">-WhatIf</span></span>
<span data-ttu-id="62641-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62641-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62641-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="62641-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62641-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62641-153">CommonParameters</span></span>
<span data-ttu-id="62641-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62641-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62641-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62641-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62641-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62641-156">INPUTS</span></span>

## <span data-ttu-id="62641-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62641-157">OUTPUTS</span></span>

### <span data-ttu-id="62641-158">Microsoft.Azure.PowerShell.Cmdlet.DesktopVirtualization.Models.Api20201102Preview.IApplication</span><span class="sxs-lookup"><span data-stu-id="62641-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201102Preview.IApplication</span></span>

## <span data-ttu-id="62641-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62641-159">NOTES</span></span>

<span data-ttu-id="62641-160">ALIASY</span><span class="sxs-lookup"><span data-stu-id="62641-160">ALIASES</span></span>

## <span data-ttu-id="62641-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62641-161">RELATED LINKS</span></span>

