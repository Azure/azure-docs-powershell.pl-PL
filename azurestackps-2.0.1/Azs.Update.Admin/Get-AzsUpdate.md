---
external help file: ''
Module Name: Azs.Update.Admin
online version: https://docs.microsoft.com/powershell/module/azs.update.admin/get-azsupdate
schema: 2.0.0
ms.openlocfilehash: d4acc60a0f5b9acc15efd66187c09ec3acb6cb62
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 06/24/2020
ms.locfileid: "94054139"
---
# <span data-ttu-id="ab272-101">Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="ab272-101">Get-AzsUpdate</span></span>

## <span data-ttu-id="ab272-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab272-102">SYNOPSIS</span></span>
<span data-ttu-id="ab272-103">Uzyskaj określoną aktualizację w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ab272-103">Get a specific update at an update location.</span></span>

## <span data-ttu-id="ab272-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab272-104">SYNTAX</span></span>

### <span data-ttu-id="ab272-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ab272-105">List (Default)</span></span>
```
Get-AzsUpdate [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ab272-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ab272-106">Get</span></span>
```
Get-AzsUpdate -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ab272-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ab272-107">GetViaIdentity</span></span>
```
Get-AzsUpdate -InputObject <IUpdateAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ab272-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ab272-108">DESCRIPTION</span></span>
<span data-ttu-id="ab272-109">Uzyskaj określoną aktualizację w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ab272-109">Get a specific update at an update location.</span></span>

## <span data-ttu-id="ab272-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab272-110">EXAMPLES</span></span>

### <span data-ttu-id="ab272-111">Przykład 1: Pobierz wszystkie aktualizacje</span><span class="sxs-lookup"><span data-stu-id="ab272-111">Example 1: Get All Updates</span></span>
```powershell
PS C:\> Get-AzsUpdate

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="ab272-112">Bez żadnych parametrów Get-AzsUpdate będą wystawiać wszystkie aktualizacje, które może wykryć stempel</span><span class="sxs-lookup"><span data-stu-id="ab272-112">Without any parameters, Get-AzsUpdate will list all updates that the stamp can discover</span></span>

### <span data-ttu-id="ab272-113">Przykład 2: uzyskaj aktualizację według nazwy</span><span class="sxs-lookup"><span data-stu-id="ab272-113">Example 2: Get Update by Name</span></span>
```powershell
PS C:\> Get-AzsUpdate -Name Microsoft1.1907.0.10
or
PS C:\> Get-AzsUpdate -Name northwest/Microsoft1.1907.0.10


Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
```

<span data-ttu-id="ab272-114">Zostaną pobrane wszystkie aktualizacje odpowiadające określonej nazwie</span><span class="sxs-lookup"><span data-stu-id="ab272-114">Will retrieve all updates that correspond to the specified Name</span></span>

### <span data-ttu-id="ab272-115">Przykład 3: pobieranie wszystkich aktualizacji według lokalizacji</span><span class="sxs-lookup"><span data-stu-id="ab272-115">Example 3: Get All Updates by Location</span></span>
```powershell
PS C:\> Get-AzsUpdate -Location northwest

Location        DisplayName                    Name                                     State                Publisher
--------        -----------                    ----                                     -----                ---------
northwest       AzS Update - 1.1907.0.10       northwest/Microsoft1.1907.0.10           Installed            Microsoft
northwest       AzS Update - 1.1907.0.13       northwest/Microsoft1.1907.0.13           Installed            Microsoft
northwest       AzS Update - 1.1907.0.20       northwest/Microsoft1.1907.0.20           Installed            Microsoft
```

<span data-ttu-id="ab272-116">Wszystkie aktualizacje zostaną pobrane w określonym miejscu.</span><span class="sxs-lookup"><span data-stu-id="ab272-116">Will retrieve all updates within a specified Location.</span></span>
<span data-ttu-id="ab272-117">Obecnie jest obsługiwana tylko jedna lokalizacja, więc jest to równoważne tylko Get-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="ab272-117">Currently, only one location is supported so this is the equivalent as just Get-AzsUpdate</span></span>

## <span data-ttu-id="ab272-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab272-118">PARAMETERS</span></span>

### <span data-ttu-id="ab272-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab272-119">-DefaultProfile</span></span>
<span data-ttu-id="ab272-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab272-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab272-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab272-121">-InputObject</span></span>
<span data-ttu-id="ab272-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="ab272-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ab272-123">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ab272-123">-Location</span></span>
<span data-ttu-id="ab272-124">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ab272-124">The name of the update location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="ab272-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ab272-125">-Name</span></span>
<span data-ttu-id="ab272-126">Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ab272-126">Name of the update.</span></span>

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

### <span data-ttu-id="ab272-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab272-127">-ResourceGroupName</span></span>
<span data-ttu-id="ab272-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab272-128">Resource group name.</span></span>

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

### <span data-ttu-id="ab272-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ab272-129">-SubscriptionId</span></span>
<span data-ttu-id="ab272-130">Poświadczenia abonamentu, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ab272-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ab272-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ab272-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="ab272-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab272-132">CommonParameters</span></span>
<span data-ttu-id="ab272-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab272-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab272-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab272-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab272-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab272-135">INPUTS</span></span>

### <span data-ttu-id="ab272-136">Microsoft. Azure. PowerShell. polecenia. UpdateAdmin. models. IUpdateAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="ab272-136">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.IUpdateAdminIdentity</span></span>

## <span data-ttu-id="ab272-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab272-137">OUTPUTS</span></span>

### <span data-ttu-id="ab272-138">Microsoft. Azure. PowerShell. polecenia. UpdateAdmin. models. Api20160501. IUpdate</span><span class="sxs-lookup"><span data-stu-id="ab272-138">Microsoft.Azure.PowerShell.Cmdlets.UpdateAdmin.Models.Api20160501.IUpdate</span></span>



## <span data-ttu-id="ab272-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab272-139">NOTES</span></span>

<span data-ttu-id="ab272-140">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="ab272-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ab272-141">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ab272-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ab272-142">INPUTobject <IUpdateAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="ab272-142">INPUTOBJECT <IUpdateAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ab272-143">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="ab272-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ab272-144">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ab272-144">`[ResourceGroupName <String>]`: Resource group name.</span></span>
  - <span data-ttu-id="ab272-145">`[RunName <String>]`: Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ab272-145">`[RunName <String>]`: Update run identifier.</span></span>
  - <span data-ttu-id="ab272-146">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ab272-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>  <span data-ttu-id="ab272-147">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="ab272-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ab272-148">`[UpdateLocation <String>]`: Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ab272-148">`[UpdateLocation <String>]`: The name of the update location.</span></span>
  - <span data-ttu-id="ab272-149">`[UpdateName <String>]`: Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ab272-149">`[UpdateName <String>]`: Name of the update.</span></span>

## <span data-ttu-id="ab272-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab272-150">RELATED LINKS</span></span>

