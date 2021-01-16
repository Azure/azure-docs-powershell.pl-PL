---
external help file: ''
Module Name: Az.DesktopVirtualization
online version: https://docs.microsoft.com/en-us/powershell/module/az.desktopvirtualization/disconnect-azwvdusersession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DesktopVirtualization/help/Disconnect-AzWvdUserSession.md
ms.openlocfilehash: 016719f32af1af9acdc4543d565f9acc086b05fa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333529"
---
# <span data-ttu-id="4df67-101">Disconnect-AzWvdUserSession</span><span class="sxs-lookup"><span data-stu-id="4df67-101">Disconnect-AzWvdUserSession</span></span>

## <span data-ttu-id="4df67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4df67-102">SYNOPSIS</span></span>
<span data-ttu-id="4df67-103">Odłączanie userSession.</span><span class="sxs-lookup"><span data-stu-id="4df67-103">Disconnect a userSession.</span></span>

## <span data-ttu-id="4df67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4df67-104">SYNTAX</span></span>

### <span data-ttu-id="4df67-105">Rozłącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4df67-105">Disconnect (Default)</span></span>
```
Disconnect-AzWvdUserSession -HostPoolName <String> -Id <String> -ResourceGroupName <String>
 -SessionHostName <String> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4df67-106">DisconnectViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4df67-106">DisconnectViaIdentity</span></span>
```
Disconnect-AzWvdUserSession -InputObject <IDesktopVirtualizationIdentity> [-DefaultProfile <PSObject>]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4df67-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4df67-107">DESCRIPTION</span></span>
<span data-ttu-id="4df67-108">Odłączanie userSession.</span><span class="sxs-lookup"><span data-stu-id="4df67-108">Disconnect a userSession.</span></span>

## <span data-ttu-id="4df67-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4df67-109">EXAMPLES</span></span>

### <span data-ttu-id="4df67-110">Przykład 1: odłączanie pulpitu wirtualnego systemu Windows UserSession według nazwy</span><span class="sxs-lookup"><span data-stu-id="4df67-110">Example 1: Disconnect a Windows Virtual Desktop UserSession by name</span></span>
```powershell
PS C:\> Disconnect-AzWvdUserSession -ResourceGroupName ResourceGroupName -HostPoolName HostPoolName -SessionHostName SessionHostName -Id 2
```

<span data-ttu-id="4df67-111">To polecenie rozłącza UserSession pulpitu wirtualnego systemu Windows na hoście sesji.</span><span class="sxs-lookup"><span data-stu-id="4df67-111">This command disconnects a Windows Virtual Desktop UserSession in a Session Host.</span></span>

## <span data-ttu-id="4df67-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4df67-112">PARAMETERS</span></span>

### <span data-ttu-id="4df67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4df67-113">-DefaultProfile</span></span>
<span data-ttu-id="4df67-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4df67-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4df67-115">-HostPoolName</span><span class="sxs-lookup"><span data-stu-id="4df67-115">-HostPoolName</span></span>
<span data-ttu-id="4df67-116">Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="4df67-116">The name of the host pool within the specified resource group</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df67-117">-ID</span><span class="sxs-lookup"><span data-stu-id="4df67-117">-Id</span></span>
<span data-ttu-id="4df67-118">Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="4df67-118">The name of the user session within the specified session host</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases: UserSessionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df67-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4df67-119">-InputObject</span></span>
<span data-ttu-id="4df67-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4df67-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity
Parameter Sets: DisconnectViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4df67-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4df67-121">-PassThru</span></span>
<span data-ttu-id="4df67-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="4df67-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4df67-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4df67-123">-ResourceGroupName</span></span>
<span data-ttu-id="4df67-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4df67-124">The name of the resource group.</span></span>
<span data-ttu-id="4df67-125">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="4df67-125">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df67-126">-SessionHostName</span><span class="sxs-lookup"><span data-stu-id="4df67-126">-SessionHostName</span></span>
<span data-ttu-id="4df67-127">Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="4df67-127">The name of the session host within the specified host pool</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df67-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4df67-128">-SubscriptionId</span></span>
<span data-ttu-id="4df67-129">Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4df67-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Disconnect
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4df67-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4df67-130">-Confirm</span></span>
<span data-ttu-id="4df67-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4df67-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4df67-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4df67-132">-WhatIf</span></span>
<span data-ttu-id="4df67-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4df67-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4df67-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4df67-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4df67-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4df67-135">CommonParameters</span></span>
<span data-ttu-id="4df67-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4df67-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4df67-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4df67-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4df67-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4df67-138">INPUTS</span></span>

### <span data-ttu-id="4df67-139">Microsoft. Azure. PowerShell. polecenia. DesktopVirtualization. models. IDesktopVirtualizationIdentity</span><span class="sxs-lookup"><span data-stu-id="4df67-139">Microsoft.Azure.PowerShell.Cmdlets.DesktopVirtualization.Models.IDesktopVirtualizationIdentity</span></span>

## <span data-ttu-id="4df67-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4df67-140">OUTPUTS</span></span>

### <span data-ttu-id="4df67-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4df67-141">System.Boolean</span></span>

## <span data-ttu-id="4df67-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4df67-142">NOTES</span></span>

<span data-ttu-id="4df67-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4df67-143">ALIASES</span></span>

<span data-ttu-id="4df67-144">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4df67-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4df67-145">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4df67-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4df67-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4df67-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4df67-147">INPUTobject <IDesktopVirtualizationIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="4df67-147">INPUTOBJECT <IDesktopVirtualizationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4df67-148">`[ApplicationGroupName <String>]`: Nazwa grupy aplikacji</span><span class="sxs-lookup"><span data-stu-id="4df67-148">`[ApplicationGroupName <String>]`: The name of the application group</span></span>
  - <span data-ttu-id="4df67-149">`[ApplicationName <String>]`: Nazwa aplikacji w określonej grupie aplikacji</span><span class="sxs-lookup"><span data-stu-id="4df67-149">`[ApplicationName <String>]`: The name of the application within the specified application group</span></span>
  - <span data-ttu-id="4df67-150">`[DesktopName <String>]`: Nazwa pulpitu w określonej grupie pulpit</span><span class="sxs-lookup"><span data-stu-id="4df67-150">`[DesktopName <String>]`: The name of the desktop within the specified desktop group</span></span>
  - <span data-ttu-id="4df67-151">`[HostPoolName <String>]`: Nazwa puli hostów w określonej grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="4df67-151">`[HostPoolName <String>]`: The name of the host pool within the specified resource group</span></span>
  - <span data-ttu-id="4df67-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4df67-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4df67-153">`[MsixPackageFullName <String>]`: Pakiet specyficzny dla wersji pełna nazwa pakietu MSIX w określonym hostpool</span><span class="sxs-lookup"><span data-stu-id="4df67-153">`[MsixPackageFullName <String>]`: The version specific package full name of the MSIX package within specified hostpool</span></span>
  - <span data-ttu-id="4df67-154">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4df67-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="4df67-155">W nazwie nie jest rozróżniana wielkość liter.</span><span class="sxs-lookup"><span data-stu-id="4df67-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="4df67-156">`[SessionHostName <String>]`: Nazwa hosta sesji w określonej puli hostów</span><span class="sxs-lookup"><span data-stu-id="4df67-156">`[SessionHostName <String>]`: The name of the session host within the specified host pool</span></span>
  - <span data-ttu-id="4df67-157">`[SubscriptionId <String>]`: Identyfikator subskrypcji docelowej.</span><span class="sxs-lookup"><span data-stu-id="4df67-157">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="4df67-158">`[UserSessionId <String>]`: Nazwa sesji użytkownika w określonym hoście sesji</span><span class="sxs-lookup"><span data-stu-id="4df67-158">`[UserSessionId <String>]`: The name of the user session within the specified session host</span></span>
  - <span data-ttu-id="4df67-159">`[WorkspaceName <String>]`: Nazwa obszaru roboczego</span><span class="sxs-lookup"><span data-stu-id="4df67-159">`[WorkspaceName <String>]`: The name of the workspace</span></span>

## <span data-ttu-id="4df67-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4df67-160">RELATED LINKS</span></span>

