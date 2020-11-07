---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890106"
---
# <span data-ttu-id="3df5a-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="3df5a-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="3df5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3df5a-102">SYNOPSIS</span></span>
<span data-ttu-id="3df5a-103">Uzyskaj lokalizację aktualizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="3df5a-103">Get an update location based on name.</span></span>

## <span data-ttu-id="3df5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3df5a-104">SYNTAX</span></span>

### <span data-ttu-id="3df5a-105">Get (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3df5a-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3df5a-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3df5a-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3df5a-107">Lista</span><span class="sxs-lookup"><span data-stu-id="3df5a-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3df5a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3df5a-108">DESCRIPTION</span></span>
<span data-ttu-id="3df5a-109">Uzyskaj lokalizację aktualizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="3df5a-109">Get an update location based on name.</span></span>

## <span data-ttu-id="3df5a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3df5a-110">EXAMPLES</span></span>

### <span data-ttu-id="3df5a-111">Przykład 1: pobieranie wszystkich lokalizacji aktualizacji</span><span class="sxs-lookup"><span data-stu-id="3df5a-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="3df5a-112">Bez żadnych parametrów ta unifiedgroup będzie pobierać wszystkie lokalizacje aktualizacji</span><span class="sxs-lookup"><span data-stu-id="3df5a-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="3df5a-113">Przykład 2: pobieranie wszystkich lokalizacji aktualizacji według nazwy</span><span class="sxs-lookup"><span data-stu-id="3df5a-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="3df5a-114">Spowoduje pobranie wszystkich lokalizacji aktualizacji zgodnych z określonym parametrem nazwy</span><span class="sxs-lookup"><span data-stu-id="3df5a-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="3df5a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3df5a-115">PARAMETERS</span></span>

### <span data-ttu-id="3df5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3df5a-116">-DefaultProfile</span></span>
<span data-ttu-id="3df5a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3df5a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3df5a-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3df5a-118">-InputObject</span></span>
<span data-ttu-id="3df5a-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3df5a-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3df5a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3df5a-120">-Name</span></span>
<span data-ttu-id="3df5a-121">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="3df5a-121">The name of the update location.</span></span>

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

### <span data-ttu-id="3df5a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3df5a-122">-ResourceGroupName</span></span>
<span data-ttu-id="3df5a-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3df5a-123">Resource group name.</span></span>

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

### <span data-ttu-id="3df5a-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3df5a-124">-SubscriptionId</span></span>
<span data-ttu-id="3df5a-125">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3df5a-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3df5a-126">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3df5a-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3df5a-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3df5a-127">CommonParameters</span></span>
<span data-ttu-id="3df5a-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3df5a-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3df5a-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3df5a-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3df5a-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3df5a-130">INPUTS</span></span>

### <span data-ttu-id="3df5a-131">Microsoft. Azure. PowerShell. polecenia. UpdateAdmin. models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3df5a-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="3df5a-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3df5a-132">OUTPUTS</span></span>

### <span data-ttu-id="3df5a-133">Microsoft. Azure. PowerShell. polecenia. UpdateAdmin. models. Api20160501. IUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="3df5a-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="3df5a-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3df5a-134">NOTES</span></span>

<span data-ttu-id="3df5a-135">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3df5a-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3df5a-136">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3df5a-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3df5a-137">INPUTobject <IUpdateAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="3df5a-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3df5a-138">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3df5a-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3df5a-139">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3df5a-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="3df5a-140">`[RunName <String>]`: Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="3df5a-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="3df5a-141">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3df5a-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="3df5a-142">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3df5a-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="3df5a-143">`[UpdateLocation <String>]`: Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="3df5a-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="3df5a-144">`[UpdateName <String>]`: Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="3df5a-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="3df5a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3df5a-145">RELATED LINKS</span></span>

