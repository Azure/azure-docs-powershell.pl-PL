---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/new-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/New-AzWvdApplication.md
ms.openlocfilehash: 7a78404c8dde734f756792b85d27d712b5c5ed69
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304800"
---
# <span data-ttu-id="98338-101">New-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="98338-101">New-AzWvdApplication</span></span>

## <span data-ttu-id="98338-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98338-102">SYNOPSIS</span></span>
<span data-ttu-id="98338-103">Tworzenie lub aktualizowanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="98338-103">Create or update an application.</span></span>

## <span data-ttu-id="98338-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98338-104">SYNTAX</span></span>

### <span data-ttu-id="98338-105">Rozszerzenie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="98338-105">CreateExpanded (Default)</span></span>
```
New-AzWvdApplication -CommandLineSetting <CommandLineSetting> -GroupName <String> -Name <String>
 -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-FilePath <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="98338-106">AppAlias</span><span class="sxs-lookup"><span data-stu-id="98338-106">AppAlias</span></span>
```
New-AzWvdApplication -AppAlias <String> -CommandLineSetting <CommandLineSetting> -GroupName <String>
 -Name <String> -ResourceGroupName <String> [-Description <String>] [-FriendlyName <String>] [-ShowInPortal]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="98338-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98338-107">DESCRIPTION</span></span>
<span data-ttu-id="98338-108">Tworzenie lub aktualizowanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="98338-108">Create or update an application.</span></span>

## <span data-ttu-id="98338-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98338-109">EXAMPLES</span></span>

### <span data-ttu-id="98338-110">Przykład 1: Tworzenie aplikacji klasycznej Windows Virtual</span><span class="sxs-lookup"><span data-stu-id="98338-110">Example 1: Create a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="98338-111">To polecenie tworzy wirtualną aplikację klasyczną systemu Windows w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="98338-111">This command creates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="98338-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98338-112">PARAMETERS</span></span>

### <span data-ttu-id="98338-113">-AppAlias</span><span class="sxs-lookup"><span data-stu-id="98338-113">-AppAlias</span></span>
<span data-ttu-id="98338-114">Alias aplikacji z elementu menu Start</span><span class="sxs-lookup"><span data-stu-id="98338-114">App Alias from start menu item</span></span>

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

### <span data-ttu-id="98338-115">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="98338-115">-CommandLineArgument</span></span>
<span data-ttu-id="98338-116">Argumenty wiersza polecenia dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="98338-116">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="98338-117">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="98338-117">-CommandLineSetting</span></span>
<span data-ttu-id="98338-118">Określa, czy ta opublikowana aplikacja może być uruchamiana z argumentami wiersza polecenia dostarczonymi przez klienta, argumenty wiersza polecenia określone w czasie publikowania lub bez argumentów wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="98338-118">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="98338-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98338-119">-DefaultProfile</span></span>
<span data-ttu-id="98338-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98338-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98338-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="98338-121">-Description</span></span>
<span data-ttu-id="98338-122">Opis aplikacji.</span><span class="sxs-lookup"><span data-stu-id="98338-122">Description of Application.</span></span>

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

### <span data-ttu-id="98338-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="98338-123">-FilePath</span></span>
<span data-ttu-id="98338-124">Określa ścieżkę pliku wykonywalnego aplikacji.</span><span class="sxs-lookup"><span data-stu-id="98338-124">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="98338-125">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="98338-125">-FriendlyName</span></span>
<span data-ttu-id="98338-126">Przyjazna nazwa aplikacji.</span><span class="sxs-lookup"><span data-stu-id="98338-126">Friendly name of Application.</span></span>

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

### <span data-ttu-id="98338-127">-GroupName</span><span class="sxs-lookup"><span data-stu-id="98338-127">-GroupName</span></span>
<span data-ttu-id="98338-128">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="98338-128">The name of the application group</span></span>

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

### <span data-ttu-id="98338-129">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="98338-129">-IconIndex</span></span>
<span data-ttu-id="98338-130">Indeks ikony.</span><span class="sxs-lookup"><span data-stu-id="98338-130">Index of the icon.</span></span>

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

### <span data-ttu-id="98338-131">-IconPath</span><span class="sxs-lookup"><span data-stu-id="98338-131">-IconPath</span></span>
<span data-ttu-id="98338-132">Ścieżka do ikony.</span><span class="sxs-lookup"><span data-stu-id="98338-132">Path to icon.</span></span>

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

### <span data-ttu-id="98338-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98338-133">-Name</span></span>
<span data-ttu-id="98338-134">Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="98338-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="98338-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98338-135">-ResourceGroupName</span></span>
<span data-ttu-id="98338-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="98338-136">The name of the resource group.</span></span>
<span data-ttu-id="98338-137">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="98338-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="98338-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="98338-138">-ShowInPortal</span></span>
<span data-ttu-id="98338-139">Określa, czy Program RemoteApp ma być pokazywany na serwerze programu dostęp w sieci Web do usług pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="98338-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="98338-140">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="98338-140">-SubscriptionId</span></span>
<span data-ttu-id="98338-141">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="98338-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="98338-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98338-142">-Confirm</span></span>
<span data-ttu-id="98338-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98338-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98338-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98338-144">-WhatIf</span></span>
<span data-ttu-id="98338-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98338-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98338-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98338-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98338-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98338-147">CommonParameters</span></span>
<span data-ttu-id="98338-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98338-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98338-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98338-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98338-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98338-150">INPUTS</span></span>

## <span data-ttu-id="98338-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98338-151">OUTPUTS</span></span>

### <span data-ttu-id="98338-152">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="98338-152">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="98338-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98338-153">NOTES</span></span>

<span data-ttu-id="98338-154">PISUJE</span><span class="sxs-lookup"><span data-stu-id="98338-154">ALIASES</span></span>

## <span data-ttu-id="98338-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98338-155">RELATED LINKS</span></span>

