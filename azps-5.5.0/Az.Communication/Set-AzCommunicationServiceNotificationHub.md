---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: aa9084f067131abb780de798dcd1af0ed8f9d235
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177787"
---
# <span data-ttu-id="73166-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="73166-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="73166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73166-102">SYNOPSIS</span></span>
<span data-ttu-id="73166-103">Łączy Centrum powiadomień Azure z tą usługą komunikacji.</span><span class="sxs-lookup"><span data-stu-id="73166-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="73166-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="73166-104">SYNTAX</span></span>

### <span data-ttu-id="73166-105">LinkExpanded (domyślne)</span><span class="sxs-lookup"><span data-stu-id="73166-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="73166-106">Link</span><span class="sxs-lookup"><span data-stu-id="73166-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="73166-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="73166-107">DESCRIPTION</span></span>
<span data-ttu-id="73166-108">Łączy Centrum powiadomień Azure z tą usługą komunikacji.</span><span class="sxs-lookup"><span data-stu-id="73166-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="73166-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="73166-109">EXAMPLES</span></span>

### <span data-ttu-id="73166-110">Przykład 1. Interakcyjne podanie szczegółów centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="73166-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="73166-111">Połączone centrum powiadomień umożliwia zasobowi ACS wysyłanie powiadomień dotyczących określonych zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="73166-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="73166-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73166-112">PARAMETERS</span></span>

### <span data-ttu-id="73166-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="73166-113">-CommunicationServiceName</span></span>
<span data-ttu-id="73166-114">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="73166-114">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="73166-115">- ConnectionString</span><span class="sxs-lookup"><span data-stu-id="73166-115">-ConnectionString</span></span>
<span data-ttu-id="73166-116">Connection string for the notification hub</span><span class="sxs-lookup"><span data-stu-id="73166-116">Connection string for the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73166-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73166-117">-DefaultProfile</span></span>
<span data-ttu-id="73166-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="73166-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73166-119">-LinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="73166-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="73166-120">Opis centrum powiadomień azure w celu utworzenia linku do usługi do komunikacji W celu skonstruowania zobacz sekcję NOTATKI dla właściwości LINKNOTIFICATIONHUBPARAMETERS I utwórz tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="73166-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters
Parameter Sets: Link
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73166-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="73166-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="73166-122">Identyfikator zasobu centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="73166-122">The resource ID of the notification hub</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73166-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73166-123">-ResourceGroupName</span></span>
<span data-ttu-id="73166-124">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="73166-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="73166-125">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="73166-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="73166-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73166-126">-SubscriptionId</span></span>
<span data-ttu-id="73166-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="73166-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="73166-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="73166-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="73166-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="73166-129">-Confirm</span></span>
<span data-ttu-id="73166-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="73166-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73166-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73166-131">-WhatIf</span></span>
<span data-ttu-id="73166-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73166-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73166-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="73166-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73166-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73166-134">CommonParameters</span></span>
<span data-ttu-id="73166-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73166-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73166-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73166-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73166-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73166-137">INPUTS</span></span>

### <span data-ttu-id="73166-138">Microsoft.Azure.PowerShell.Cmdlet.Communication.Models.Api200820Preview.ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="73166-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="73166-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73166-139">OUTPUTS</span></span>

### <span data-ttu-id="73166-140">System.String</span><span class="sxs-lookup"><span data-stu-id="73166-140">System.String</span></span>

## <span data-ttu-id="73166-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="73166-141">NOTES</span></span>

<span data-ttu-id="73166-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="73166-142">ALIASES</span></span>

<span data-ttu-id="73166-143">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="73166-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73166-144">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="73166-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73166-145">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73166-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73166-146">LINKNOTIFICATIONHUBPARAMETERS: Opis centrum powiadomień platformy Azure w <ILinkNotificationHubParameters> celu połączenia z usługą komunikacji</span><span class="sxs-lookup"><span data-stu-id="73166-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="73166-147">`ConnectionString <String>`: parametrów połączenia dla centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="73166-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="73166-148">`ResourceId <String>`: Identyfikator zasobu centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="73166-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="73166-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73166-149">RELATED LINKS</span></span>

