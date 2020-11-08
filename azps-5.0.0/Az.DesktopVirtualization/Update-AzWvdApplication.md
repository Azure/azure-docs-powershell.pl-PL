---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/update-azwvdapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Update-AzWvdApplication.md
ms.openlocfilehash: 8c2026e7ef8ed5c0eeb1e5a4cb7f605c1a030b9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231958"
---
# <span data-ttu-id="a0ca2-101">Update-AzWvdApplication</span><span class="sxs-lookup"><span data-stu-id="a0ca2-101">Update-AzWvdApplication</span></span>

## <span data-ttu-id="a0ca2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="a0ca2-103">Aktualizowanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-103">Update an application.</span></span>

## <span data-ttu-id="a0ca2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0ca2-104">SYNTAX</span></span>

### <span data-ttu-id="a0ca2-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a0ca2-105">UpdateExpanded (Default)</span></span>
```
Update-AzWvdApplication -GroupName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-CommandLineArgument <String>] [-CommandLineSetting <CommandLineSetting>]
 [-Description <String>] [-FilePath <String>] [-FriendlyName <String>] [-IconIndex <Int32>]
 [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a0ca2-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a0ca2-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzWvdApplication -InputObject <IDesktopVirtualizationIdentity> [-CommandLineArgument <String>]
 [-CommandLineSetting <CommandLineSetting>] [-Description <String>] [-FilePath <String>]
 [-FriendlyName <String>] [-IconIndex <Int32>] [-IconPath <String>] [-ShowInPortal] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a0ca2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a0ca2-107">DESCRIPTION</span></span>
<span data-ttu-id="a0ca2-108">Aktualizowanie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-108">Update an application.</span></span>

## <span data-ttu-id="a0ca2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0ca2-109">EXAMPLES</span></span>

### <span data-ttu-id="a0ca2-110">Przykład 1: aktualizowanie aplikacji klasycznej Windows Virtual</span><span class="sxs-lookup"><span data-stu-id="a0ca2-110">Example 1: Update a Windows Virtual Desktop Application</span></span>
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

<span data-ttu-id="a0ca2-111">To polecenie aktualizuje aplikację klasyczną systemu Windows w grupie Applicaton.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-111">This command updates a Windows Virtual Desktop Application in an applicaton Group.</span></span>

## <span data-ttu-id="a0ca2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0ca2-112">PARAMETERS</span></span>

### <span data-ttu-id="a0ca2-113">-CommandLineArgument</span><span class="sxs-lookup"><span data-stu-id="a0ca2-113">-CommandLineArgument</span></span>
<span data-ttu-id="a0ca2-114">Argumenty wiersza polecenia dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-114">Command Line Arguments for Application.</span></span>

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

### <span data-ttu-id="a0ca2-115">-CommandLineSetting</span><span class="sxs-lookup"><span data-stu-id="a0ca2-115">-CommandLineSetting</span></span>
<span data-ttu-id="a0ca2-116">Określa, czy ta opublikowana aplikacja może być uruchamiana z argumentami wiersza polecenia dostarczonymi przez klienta, argumenty wiersza polecenia określone w czasie publikowania lub bez argumentów wiersza polecenia.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-116">Specifies whether this published application can be launched with command line arguments provided by the client, command line arguments specified at publish time, or no command line arguments at all.</span></span>

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

### <span data-ttu-id="a0ca2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0ca2-117">-DefaultProfile</span></span>
<span data-ttu-id="a0ca2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0ca2-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="a0ca2-119">-Description</span></span>
<span data-ttu-id="a0ca2-120">Opis aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-120">Description of Application.</span></span>

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

### <span data-ttu-id="a0ca2-121">-FilePath</span><span class="sxs-lookup"><span data-stu-id="a0ca2-121">-FilePath</span></span>
<span data-ttu-id="a0ca2-122">Określa ścieżkę pliku wykonywalnego aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-122">Specifies a path for the executable file for the application.</span></span>

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

### <span data-ttu-id="a0ca2-123">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a0ca2-123">-FriendlyName</span></span>
<span data-ttu-id="a0ca2-124">Przyjazna nazwa aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-124">Friendly name of Application.</span></span>

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

### <span data-ttu-id="a0ca2-125">-GroupName</span><span class="sxs-lookup"><span data-stu-id="a0ca2-125">-GroupName</span></span>
<span data-ttu-id="a0ca2-126">Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a0ca2-126">The name of the application group</span></span>

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

### <span data-ttu-id="a0ca2-127">-IconIndex</span><span class="sxs-lookup"><span data-stu-id="a0ca2-127">-IconIndex</span></span>
<span data-ttu-id="a0ca2-128">Indeks ikony.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-128">Index of the icon.</span></span>

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

### <span data-ttu-id="a0ca2-129">-IconPath</span><span class="sxs-lookup"><span data-stu-id="a0ca2-129">-IconPath</span></span>
<span data-ttu-id="a0ca2-130">Ścieżka do ikony.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-130">Path to icon.</span></span>

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

### <span data-ttu-id="a0ca2-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0ca2-131">-InputObject</span></span>
<span data-ttu-id="a0ca2-132">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-132">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a0ca2-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0ca2-133">-Name</span></span>
<span data-ttu-id="a0ca2-134">Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="a0ca2-134">The name of the application within the specified application group</span></span>

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

### <span data-ttu-id="a0ca2-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0ca2-135">-ResourceGroupName</span></span>
<span data-ttu-id="a0ca2-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-136">The name of the resource group.</span></span>
<span data-ttu-id="a0ca2-137">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-137">The name is case insensitive.</span></span>

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

### <span data-ttu-id="a0ca2-138">-ShowInPortal</span><span class="sxs-lookup"><span data-stu-id="a0ca2-138">-ShowInPortal</span></span>
<span data-ttu-id="a0ca2-139">Określa, czy Program RemoteApp ma być pokazywany na serwerze programu dostęp w sieci Web do usług pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-139">Specifies whether to show the RemoteApp program in the RD Web Access server.</span></span>

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

### <span data-ttu-id="a0ca2-140">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a0ca2-140">-SubscriptionId</span></span>
<span data-ttu-id="a0ca2-141">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-141">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="a0ca2-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0ca2-142">-Tag</span></span>
<span data-ttu-id="a0ca2-143">Tagi do zaktualizowania</span><span class="sxs-lookup"><span data-stu-id="a0ca2-143">tags to be updated</span></span>

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

### <span data-ttu-id="a0ca2-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0ca2-144">-Confirm</span></span>
<span data-ttu-id="a0ca2-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0ca2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0ca2-146">-WhatIf</span></span>
<span data-ttu-id="a0ca2-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0ca2-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0ca2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0ca2-149">CommonParameters</span></span>
<span data-ttu-id="a0ca2-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0ca2-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0ca2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0ca2-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0ca2-152">INPUTS</span></span>

### <span data-ttu-id="a0ca2-153">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="a0ca2-153">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="a0ca2-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0ca2-154">OUTPUTS</span></span>

### <span data-ttu-id="a0ca2-155">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. Api20191210Preview. IApplication</span><span class="sxs-lookup"><span data-stu-id="a0ca2-155">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.Api20191210Preview.IApplication</span></span>

## <span data-ttu-id="a0ca2-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0ca2-156">NOTES</span></span>

<span data-ttu-id="a0ca2-157">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a0ca2-157">ALIASES</span></span>

<span data-ttu-id="a0ca2-158">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0ca2-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a0ca2-159">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a0ca2-160">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a0ca2-161">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a0ca2-161">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a0ca2-162">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="a0ca2-162">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="a0ca2-163">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="a0ca2-163">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="a0ca2-164">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="a0ca2-164">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="a0ca2-165">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="a0ca2-165">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="a0ca2-166">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a0ca2-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a0ca2-167">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-167">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="a0ca2-168">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-168">The name is case insensitive.</span></span>
  - <span data-ttu-id="a0ca2-169">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="a0ca2-169">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="a0ca2-170">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="a0ca2-170">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="a0ca2-171">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="a0ca2-171">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="a0ca2-172">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="a0ca2-172">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="a0ca2-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0ca2-173">RELATED LINKS</span></span>

