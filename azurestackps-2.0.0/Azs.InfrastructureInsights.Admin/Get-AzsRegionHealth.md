---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregionhealth
schema: 2.0.0
ms.openlocfilehash: 6f5fa25f1b35ac03d27688eced71919cb409d1cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893962"
---
# <span data-ttu-id="f4666-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="f4666-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="f4666-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4666-102">SYNOPSIS</span></span>
<span data-ttu-id="f4666-103">Zwraca żądany stan kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="f4666-103">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="f4666-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4666-104">SYNTAX</span></span>

### <span data-ttu-id="f4666-105">Get (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f4666-105">Get (Default)</span></span>
```
Get-AzsRegionHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f4666-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f4666-106">GetViaIdentity</span></span>
```
Get-AzsRegionHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f4666-107">Lista</span><span class="sxs-lookup"><span data-stu-id="f4666-107">List</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f4666-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f4666-108">DESCRIPTION</span></span>
<span data-ttu-id="f4666-109">Zwraca żądany stan kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="f4666-109">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="f4666-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4666-110">EXAMPLES</span></span>

### <span data-ttu-id="f4666-111">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="f4666-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegionHealth
```

<span data-ttu-id="f4666-112">Zwraca listę stanów kondycji regionu.</span><span class="sxs-lookup"><span data-stu-id="f4666-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="f4666-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4666-113">PARAMETERS</span></span>

### <span data-ttu-id="f4666-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4666-114">-DefaultProfile</span></span>
<span data-ttu-id="f4666-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4666-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4666-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="f4666-116">-Filter</span></span>
<span data-ttu-id="f4666-117">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="f4666-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4666-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f4666-118">-InputObject</span></span>
<span data-ttu-id="f4666-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="f4666-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="f4666-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f4666-120">-Location</span></span>
<span data-ttu-id="f4666-121">Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="f4666-121">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4666-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4666-122">-ResourceGroupName</span></span>
<span data-ttu-id="f4666-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4666-123">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4666-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f4666-124">-SubscriptionId</span></span>
<span data-ttu-id="f4666-125">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f4666-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f4666-126">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f4666-126">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f4666-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4666-127">CommonParameters</span></span>
<span data-ttu-id="f4666-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4666-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4666-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4666-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4666-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4666-130">INPUTS</span></span>

### <span data-ttu-id="f4666-131">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f4666-131">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="f4666-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4666-132">OUTPUTS</span></span>

### <span data-ttu-id="f4666-133">Microsoft. Azure. PowerShell. polecenia. InfrastructureInsightsAdmin. models. Api20160501. IRegionHealth</span><span class="sxs-lookup"><span data-stu-id="f4666-133">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IRegionHealth</span></span>



## <span data-ttu-id="f4666-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4666-134">NOTES</span></span>

<span data-ttu-id="f4666-135">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="f4666-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f4666-136">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f4666-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f4666-137">INPUTobject <IInfrastructureInsightsAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="f4666-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f4666-138">`[AlertName <String>]`: Nazwa alertu.</span><span class="sxs-lookup"><span data-stu-id="f4666-138">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="f4666-139">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="f4666-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f4666-140">`[Location <String>]`: Nazwa regionu</span><span class="sxs-lookup"><span data-stu-id="f4666-140">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="f4666-141">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f4666-141">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="f4666-142">`[ResourceRegistrationId <String>]`: Identyfikator rejestracji zasobu.</span><span class="sxs-lookup"><span data-stu-id="f4666-142">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="f4666-143">`[ServiceHealth <String>]`: Nazwa kondycji usługi.</span><span class="sxs-lookup"><span data-stu-id="f4666-143">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="f4666-144">`[ServiceRegistrationId <String>]`: Identyfikator rejestracji usługi.</span><span class="sxs-lookup"><span data-stu-id="f4666-144">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="f4666-145">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="f4666-145">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f4666-146">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="f4666-146">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="f4666-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4666-147">RELATED LINKS</span></span>

