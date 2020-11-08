---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdatelocation
schema: 2.0.0
ms.openlocfilehash: 0aa8e2358a5af4a5f73339a1068b0668914eef6e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055708"
---
# <span data-ttu-id="dddc7-101">Get-AzsUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="dddc7-101">Get-AzsUpdateLocation</span></span>

## <span data-ttu-id="dddc7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dddc7-102">SYNOPSIS</span></span>
<span data-ttu-id="dddc7-103">Uzyskaj lokalizację aktualizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="dddc7-103">Get an update location based on name.</span></span>

## <span data-ttu-id="dddc7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dddc7-104">SYNTAX</span></span>

### <span data-ttu-id="dddc7-105">Get (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="dddc7-105">Get (Default)</span></span>
```
Get-AzsUpdateLocation [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dddc7-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dddc7-106">GetViaIdentity</span></span>
```
Get-AzsUpdateLocation -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dddc7-107">Lista</span><span class="sxs-lookup"><span data-stu-id="dddc7-107">List</span></span>
```
Get-AzsUpdateLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="dddc7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dddc7-108">DESCRIPTION</span></span>
<span data-ttu-id="dddc7-109">Uzyskaj lokalizację aktualizacji na podstawie nazwy.</span><span class="sxs-lookup"><span data-stu-id="dddc7-109">Get an update location based on name.</span></span>

## <span data-ttu-id="dddc7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dddc7-110">EXAMPLES</span></span>

### <span data-ttu-id="dddc7-111">Przykład 1: pobieranie wszystkich lokalizacji aktualizacji</span><span class="sxs-lookup"><span data-stu-id="dddc7-111">Example 1: Get All Updates Locations</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="dddc7-112">Bez żadnych parametrów ta unifiedgroup będzie pobierać wszystkie lokalizacje aktualizacji</span><span class="sxs-lookup"><span data-stu-id="dddc7-112">Without any parameters, this commandlet will retrieve all update locations</span></span>

### <span data-ttu-id="dddc7-113">Przykład 2: pobieranie wszystkich lokalizacji aktualizacji według nazwy</span><span class="sxs-lookup"><span data-stu-id="dddc7-113">Example 2: Get All Updates Locations by Name</span></span>
```powershell
PS C:\> Get-AzsUpdateLocation -Name northwest

Name                 CurrentVersion       CurrentOemVersion    State
----                 --------------       -----------------    -----
northwest            1.1912.0.30          2.1.1907.4           AppliedSuccessfully
```

<span data-ttu-id="dddc7-114">Spowoduje pobranie wszystkich lokalizacji aktualizacji zgodnych z określonym parametrem nazwy</span><span class="sxs-lookup"><span data-stu-id="dddc7-114">Will retrieve all update locations that matches the specified Name parameter</span></span>

## <span data-ttu-id="dddc7-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dddc7-115">PARAMETERS</span></span>

### <span data-ttu-id="dddc7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dddc7-116">-DefaultProfile</span></span>
<span data-ttu-id="dddc7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dddc7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dddc7-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dddc7-118">-InputObject</span></span>
<span data-ttu-id="dddc7-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="dddc7-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dddc7-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dddc7-120">-Name</span></span>
<span data-ttu-id="dddc7-121">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="dddc7-121">The name of the update location.</span></span>

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

### <span data-ttu-id="dddc7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dddc7-122">-ResourceGroupName</span></span>
<span data-ttu-id="dddc7-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dddc7-123">Resource group name.</span></span>

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

### <span data-ttu-id="dddc7-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dddc7-124">-SubscriptionId</span></span>
<span data-ttu-id="dddc7-125">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dddc7-125">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dddc7-126">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="dddc7-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dddc7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dddc7-127">CommonParameters</span></span>
<span data-ttu-id="dddc7-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dddc7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dddc7-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dddc7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dddc7-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dddc7-130">INPUTS</span></span>

### <span data-ttu-id="dddc7-131">Microsoft. Azure. PowerShell. polecenia. UpdateAdmin. models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="dddc7-131">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="dddc7-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dddc7-132">OUTPUTS</span></span>

### <span data-ttu-id="dddc7-133">Microsoft. Azure. PowerShell. polecenia. UpdateAdmin. models. Api20160501. IUpdateLocation</span><span class="sxs-lookup"><span data-stu-id="dddc7-133">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdateLocation</span></span>



## <span data-ttu-id="dddc7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dddc7-134">NOTES</span></span>

<span data-ttu-id="dddc7-135">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="dddc7-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dddc7-136">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dddc7-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dddc7-137">INPUTobject <IUpdateAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="dddc7-137">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dddc7-138">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="dddc7-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dddc7-139">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dddc7-139">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="dddc7-140">`[RunName <String>]`: Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="dddc7-140">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="dddc7-141">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dddc7-141">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="dddc7-142">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="dddc7-142">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dddc7-143">`[UpdateLocation <String>]`: Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="dddc7-143">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="dddc7-144">`[UpdateName <String>]`: Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="dddc7-144">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="dddc7-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dddc7-145">RELATED LINKS</span></span>

