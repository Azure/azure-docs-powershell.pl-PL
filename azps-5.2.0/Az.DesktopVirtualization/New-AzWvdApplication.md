---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 724e1877b924829560112f926b75bd1c523c8f18
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341422"
---
# <span data-ttu-id="42ae8-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="42ae8-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="42ae8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42ae8-102">SYNOPSIS</span></span>
<span data-ttu-id="42ae8-103">Tworzenie lub aktualizowanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="42ae8-103">Create or update an application.</span></span>

## <span data-ttu-id="42ae8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42ae8-104">SYNTAX</span></span>

### <span data-ttu-id="42ae8-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="42ae8-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-ApplicationType <RemoteApplicationType>] [-CommandLineArgument <String>]
 [-FilePath <String>] [-IconIndex <Int32>] [-IconPath <String>] [-MsixPackageApplicationId <String>]
 [-MsixPackageFamilyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="42ae8-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="42ae8-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="42ae8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="42ae8-107">DESCRIPTION</span></span>
<span data-ttu-id="42ae8-108">Tworzenie lub aktualizowanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="42ae8-108">Create or update an application.</span></span>

## <span data-ttu-id="42ae8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42ae8-109">EXAMPLES</span></span>

### <span data-ttu-id="42ae8-110">Przykład 1: Tworzenie aplikacji klasycznej Windows Virtual</span><span class="sxs-lookup"><span data-stu-id="42ae8-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="42ae8-111">To polecenie tworzy wirtualną aplikację klasyczną systemu Windows w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="42ae8-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="42ae8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42ae8-112">PARAMETERS</span></span>

### <span data-ttu-id="42ae8-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="42ae8-113">-AppAlias</span></span>
<span data-ttu-id="42ae8-114">Alias aplikacji z elementu menu Start</span><span class="sxs-lookup"><span data-stu-id="42ae8-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="42ae8-115">-ApplicationType</span><span class="sxs-lookup"><span data-stu-id="42ae8-115">-ApplicationType</span></span>
<span data-ttu-id="42ae8-116">Typ zasobu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="42ae8-116">Resource Type of Application.</span></span>

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

### <span data-ttu-id="42ae8-117">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="42ae8-117">-CommandLineArgument</span></span>
<span data-ttu-id="42ae8-118">Argumenty wiersza polecenia dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="42ae8-118">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="42ae8-119">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="42ae8-119">-CommandLineSetting</span></span>
<span data-ttu-id="42ae8-120">Określa, czy ta opublikowana aplikacja może być uruchamiana z argumentami wiersza polecenia dostarczonymi przez klienta, argumenty wiersza polecenia określone w czasie publikowania lub bez argumentów wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="42ae8-120">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="42ae8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42ae8-121">-DefaultProfile</span></span>
<span data-ttu-id="42ae8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="42ae8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42ae8-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="42ae8-123">-Description</span></span>
<span data-ttu-id="42ae8-124">Opis aplikacji.</span><span class="sxs-lookup"><span data-stu-id="42ae8-124">Description of Application.</span></span>

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

### <span data-ttu-id="42ae8-125">-FilePath</span><span class="sxs-lookup"><span data-stu-id="42ae8-125">-FilePath</span></span>
<span data-ttu-id="42ae8-126">Określa ścieżkę pliku wykonywalnego aplikacji.</span><span class="sxs-lookup"><span data-stu-id="42ae8-126">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="42ae8-127">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="42ae8-127">-FriendlyName</span></span>
<span data-ttu-id="42ae8-128">Przyjazna nazwa aplikacji.</span><span class="sxs-lookup"><span data-stu-id="42ae8-128">Friendly name of Application.</span></span>

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

### <span data-ttu-id="42ae8-129">-GroupName</span><span class="sxs-lookup"><span data-stu-id="42ae8-129">-GroupName</span></span>
<span data-ttu-id="42ae8-130">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="42ae8-130">The name of the application group</span></span>

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

### <span data-ttu-id="42ae8-131">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="42ae8-131">-IconIndex</span></span>
<span data-ttu-id="42ae8-132">Indeks ikony.</span><span class="sxs-lookup"><span data-stu-id="42ae8-132">Index of the icon.</span></span>

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

### <span data-ttu-id="42ae8-133">-IconPath</span><span class="sxs-lookup"><span data-stu-id="42ae8-133">-IconPath</span></span>
<span data-ttu-id="42ae8-134">Ścieżka do ikony.</span><span class="sxs-lookup"><span data-stu-id="42ae8-134">Path to icon.</span></span>

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

### <span data-ttu-id="42ae8-135">-MsixPackageApplicationId</span><span class="sxs-lookup"><span data-stu-id="42ae8-135">-MsixPackageApplicationId</span></span>
<span data-ttu-id="42ae8-136">Określa identyfikator aplikacji pakietu dla aplikacji MSIX</span><span class="sxs-lookup"><span data-stu-id="42ae8-136">Specifies the package application Id for MSIX applications</span></span>

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

### <span data-ttu-id="42ae8-137">-MsixPackageFamilyName</span><span class="sxs-lookup"><span data-stu-id="42ae8-137">-MsixPackageFamilyName</span></span>
<span data-ttu-id="42ae8-138">Określa nazwę rodziny pakietów dla aplikacji MSIX</span><span class="sxs-lookup"><span data-stu-id="42ae8-138">Specifies the package family name for MSIX applications</span></span>

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

### <span data-ttu-id="42ae8-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42ae8-139">-Name</span></span>
<span data-ttu-id="42ae8-140">Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="42ae8-140">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="42ae8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42ae8-141">-ResourceGroupName</span></span>
<span data-ttu-id="42ae8-142">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="42ae8-142">The name of the resource group.</span></span>
<span data-ttu-id="42ae8-143">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="42ae8-143">The name is case insensitive.</span></span>

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

### <span data-ttu-id="42ae8-144">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="42ae8-144">-ShowInPortal</span></span>
<span data-ttu-id="42ae8-145">Określa, czy Program RemoteApp ma być pokazywany na serwerze programu dostęp w sieci Web do usług pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="42ae8-145">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="42ae8-146">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="42ae8-146">-SubscriptionId</span></span>
<span data-ttu-id="42ae8-147">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="42ae8-147">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="42ae8-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42ae8-148">-Confirm</span></span>
<span data-ttu-id="42ae8-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42ae8-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42ae8-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42ae8-150">-WhatIf</span></span>
<span data-ttu-id="42ae8-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42ae8-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42ae8-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="42ae8-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42ae8-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42ae8-153">CommonParameters</span></span>
<span data-ttu-id="42ae8-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42ae8-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42ae8-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="42ae8-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42ae8-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42ae8-156">INPUTS</span></span>

## <span data-ttu-id="42ae8-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42ae8-157">OUTPUTS</span></span>

### <span data-ttu-id="42ae8-158">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20201019Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="42ae8-158">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20201019Preview.IApplication</span></span>

## <span data-ttu-id="42ae8-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42ae8-159">NOTES</span></span>

<span data-ttu-id="42ae8-160">PISUJE</span><span class="sxs-lookup"><span data-stu-id="42ae8-160">ALIASES</span></span>

## <span data-ttu-id="42ae8-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42ae8-161">RELATED LINKS</span></span>

