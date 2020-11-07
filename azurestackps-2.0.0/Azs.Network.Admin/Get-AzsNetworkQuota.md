---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkquota
schema: 2.0.0
ms.openlocfilehash: e9fbcb04841c08fe396cc56d92acd0abdaf94089
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891686"
---
# <span data-ttu-id="0cfd3-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="0cfd3-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="0cfd3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0cfd3-102">SYNOPSIS</span></span>
<span data-ttu-id="0cfd3-103">Uzyskaj przydział według nazwy.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-103">Get a quota by name.</span></span>

## <span data-ttu-id="0cfd3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0cfd3-104">SYNTAX</span></span>

### <span data-ttu-id="0cfd3-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="0cfd3-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0cfd3-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="0cfd3-106">Get</span></span>
```
Get-AzsNetworkQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0cfd3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0cfd3-107">GetViaIdentity</span></span>
```
Get-AzsNetworkQuota -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="0cfd3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0cfd3-108">DESCRIPTION</span></span>
<span data-ttu-id="0cfd3-109">Lista wszystkich przydziałów.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-109">List all quotas.</span></span>
<span data-ttu-id="0cfd3-110">Ograniczanie listy przez przekazanie nazwy lub filtru.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="0cfd3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0cfd3-111">EXAMPLES</span></span>

### <span data-ttu-id="0cfd3-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0cfd3-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="0cfd3-113">Wyświetla listę wszystkich przydziałów sieci.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="0cfd3-114">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0cfd3-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="0cfd3-115">Pobiera określony przydział sieci.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-115">Gets the specified network quota.</span></span>



## <span data-ttu-id="0cfd3-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0cfd3-116">PARAMETERS</span></span>

### <span data-ttu-id="0cfd3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cfd3-117">-DefaultProfile</span></span>
<span data-ttu-id="0cfd3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0cfd3-119">-Filter</span><span class="sxs-lookup"><span data-stu-id="0cfd3-119">-Filter</span></span>
<span data-ttu-id="0cfd3-120">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-120">OData filter parameter.</span></span>

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

### <span data-ttu-id="0cfd3-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0cfd3-121">-InputObject</span></span>
<span data-ttu-id="0cfd3-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="0cfd3-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0cfd3-123">-Location</span></span>
<span data-ttu-id="0cfd3-124">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Name
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0cfd3-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0cfd3-125">-Name</span></span>
<span data-ttu-id="0cfd3-126">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-126">Name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="0cfd3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cfd3-127">-PassThru</span></span>
<span data-ttu-id="0cfd3-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0cfd3-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0cfd3-129">-SubscriptionId</span></span>
<span data-ttu-id="0cfd3-130">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0cfd3-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0cfd3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cfd3-132">CommonParameters</span></span>
<span data-ttu-id="0cfd3-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cfd3-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0cfd3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cfd3-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cfd3-135">INPUTS</span></span>

### <span data-ttu-id="0cfd3-136">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0cfd3-136">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="0cfd3-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0cfd3-137">OUTPUTS</span></span>

### <span data-ttu-id="0cfd3-138">Microsoft. Azure. PowerShell. polecenia. NetworkAdmin. models. Api20150615. IQuota</span><span class="sxs-lookup"><span data-stu-id="0cfd3-138">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IQuota</span></span>



## <span data-ttu-id="0cfd3-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0cfd3-139">NOTES</span></span>

<span data-ttu-id="0cfd3-140">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0cfd3-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0cfd3-142">INPUTobject <INetworkAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="0cfd3-142">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0cfd3-143">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="0cfd3-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0cfd3-144">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="0cfd3-145">`[ResourceName <String>]`: Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-145">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="0cfd3-146">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0cfd3-147">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="0cfd3-147">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="0cfd3-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cfd3-148">RELATED LINKS</span></span>

