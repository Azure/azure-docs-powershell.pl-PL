---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/set-azcommunicationservicenotificationhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Set-AzCommunicationServiceNotificationHub.md
ms.openlocfilehash: aa9084f067131abb780de798dcd1af0ed8f9d235
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501965"
---
# <span data-ttu-id="116e0-101">Set-AzCommunicationServiceNotificationHub</span><span class="sxs-lookup"><span data-stu-id="116e0-101">Set-AzCommunicationServiceNotificationHub</span></span>

## <span data-ttu-id="116e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="116e0-102">SYNOPSIS</span></span>
<span data-ttu-id="116e0-103">Łączy centrum powiadomień platformy Azure z tą usługą komunikacyjną.</span><span class="sxs-lookup"><span data-stu-id="116e0-103">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="116e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="116e0-104">SYNTAX</span></span>

### <span data-ttu-id="116e0-105">LinkExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="116e0-105">LinkExpanded (Default)</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -ConnectionString <String> -NotificationHubResourceId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="116e0-106">Łącze</span><span class="sxs-lookup"><span data-stu-id="116e0-106">Link</span></span>
```
Set-AzCommunicationServiceNotificationHub -CommunicationServiceName <String> -ResourceGroupName <String>
 -LinkNotificationHubParameter <ILinkNotificationHubParameters> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="116e0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="116e0-107">DESCRIPTION</span></span>
<span data-ttu-id="116e0-108">Łączy centrum powiadomień platformy Azure z tą usługą komunikacyjną.</span><span class="sxs-lookup"><span data-stu-id="116e0-108">Links an Azure Notification Hub to this communication service.</span></span>

## <span data-ttu-id="116e0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="116e0-109">EXAMPLES</span></span>

### <span data-ttu-id="116e0-110">Przykład 1: udostępnianie szczegółów centrum powiadomień interaktywnie</span><span class="sxs-lookup"><span data-stu-id="116e0-110">Example 1: Provide Notification Hub details interactively</span></span>
```powershell
PS C:\> Set-AzCommunicationServiceNotificationHub -CommunicationServiceName ContosoAcsResource2 -ResourceGroupName ContosoResourceProvider1 -ConnectionString "<notificationhub-connectionstring>" -NotificationHubResourceId "<notificationhub-resourceid>"
```

<span data-ttu-id="116e0-111">Połączony centrum powiadomień umożliwia zasobowi ACS wysłanie powiadomień dotyczących określonych wydarzeń.</span><span class="sxs-lookup"><span data-stu-id="116e0-111">A linked notification hub allows a ACS resource to send notifications for certain events.</span></span>

## <span data-ttu-id="116e0-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="116e0-112">PARAMETERS</span></span>

### <span data-ttu-id="116e0-113">-CommunicationServiceName</span><span class="sxs-lookup"><span data-stu-id="116e0-113">-CommunicationServiceName</span></span>
<span data-ttu-id="116e0-114">Nazwa zasobu CommunicationService.</span><span class="sxs-lookup"><span data-stu-id="116e0-114">The name of the CommunicationService resource.</span></span>

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

### <span data-ttu-id="116e0-115">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="116e0-115">-ConnectionString</span></span>
<span data-ttu-id="116e0-116">Parametry połączenia dla centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="116e0-116">Connection string for the notification hub</span></span>

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

### <span data-ttu-id="116e0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116e0-117">-DefaultProfile</span></span>
<span data-ttu-id="116e0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="116e0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="116e0-119">-LinkNotificationHubParameter</span><span class="sxs-lookup"><span data-stu-id="116e0-119">-LinkNotificationHubParameter</span></span>
<span data-ttu-id="116e0-120">Opis centrum powiadomień platformy Azure aby utworzyć link do usługi komunikacyjnej do konstruowania, zobacz sekcja notatki dla właściwości LINKNOTIFICATIONHUBPARAMETER i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="116e0-120">Description of an Azure Notification Hub to link to the communication service To construct, see NOTES section for LINKNOTIFICATIONHUBPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="116e0-121">-NotificationHubResourceId</span><span class="sxs-lookup"><span data-stu-id="116e0-121">-NotificationHubResourceId</span></span>
<span data-ttu-id="116e0-122">Identyfikator zasobu centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="116e0-122">The resource ID of the notification hub</span></span>

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

### <span data-ttu-id="116e0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="116e0-123">-ResourceGroupName</span></span>
<span data-ttu-id="116e0-124">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="116e0-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="116e0-125">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="116e0-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="116e0-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="116e0-126">-SubscriptionId</span></span>
<span data-ttu-id="116e0-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="116e0-127">Gets subscription ID which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="116e0-128">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="116e0-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="116e0-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="116e0-129">-Confirm</span></span>
<span data-ttu-id="116e0-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="116e0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="116e0-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="116e0-131">-WhatIf</span></span>
<span data-ttu-id="116e0-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="116e0-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="116e0-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="116e0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="116e0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116e0-134">CommonParameters</span></span>
<span data-ttu-id="116e0-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="116e0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116e0-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="116e0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116e0-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="116e0-137">INPUTS</span></span>

### <span data-ttu-id="116e0-138">Microsoft. Azure. PowerShell. cmdlet. Communication. models. Api20200820Preview. ILinkNotificationHubParameters</span><span class="sxs-lookup"><span data-stu-id="116e0-138">Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.Api20200820Preview.ILinkNotificationHubParameters</span></span>

## <span data-ttu-id="116e0-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="116e0-139">OUTPUTS</span></span>

### <span data-ttu-id="116e0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="116e0-140">System.String</span></span>

## <span data-ttu-id="116e0-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="116e0-141">NOTES</span></span>

<span data-ttu-id="116e0-142">PISUJE</span><span class="sxs-lookup"><span data-stu-id="116e0-142">ALIASES</span></span>

<span data-ttu-id="116e0-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="116e0-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="116e0-144">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="116e0-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="116e0-145">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="116e0-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="116e0-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters> : Opis centrum powiadomień platformy Azure w celu utworzenia linku do usługi komunikacyjnej</span><span class="sxs-lookup"><span data-stu-id="116e0-146">LINKNOTIFICATIONHUBPARAMETER <ILinkNotificationHubParameters>: Description of an Azure Notification Hub to link to the communication service</span></span>
  - <span data-ttu-id="116e0-147">`ConnectionString <String>`: Parametry połączenia dla centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="116e0-147">`ConnectionString <String>`: Connection string for the notification hub</span></span>
  - <span data-ttu-id="116e0-148">`ResourceId <String>`: Identyfikator zasobu centrum powiadomień</span><span class="sxs-lookup"><span data-stu-id="116e0-148">`ResourceId <String>`: The resource ID of the notification hub</span></span>

## <span data-ttu-id="116e0-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="116e0-149">RELATED LINKS</span></span>

