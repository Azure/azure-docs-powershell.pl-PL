---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 715234586df8383a2983b4f0459ae91ca457d684
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93894009"
---
# <span data-ttu-id="935e6-101">Remove-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="935e6-101">Remove-AzsComputeQuota</span></span>

## <span data-ttu-id="935e6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="935e6-102">SYNOPSIS</span></span>
<span data-ttu-id="935e6-103">Usuń istniejący przydział obliczeń.</span><span class="sxs-lookup"><span data-stu-id="935e6-103">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="935e6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="935e6-104">SYNTAX</span></span>

### <span data-ttu-id="935e6-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="935e6-105">Delete (Default)</span></span>
```
Remove-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="935e6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="935e6-106">DeleteViaIdentity</span></span>
```
Remove-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="935e6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="935e6-107">DESCRIPTION</span></span>
<span data-ttu-id="935e6-108">Usuń istniejący przydział obliczeń.</span><span class="sxs-lookup"><span data-stu-id="935e6-108">Delete an existing Compute quota.</span></span>

## <span data-ttu-id="935e6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="935e6-109">EXAMPLES</span></span>

### <span data-ttu-id="935e6-110">Przykład 1. Usuń przydział obliczania</span><span class="sxs-lookup"><span data-stu-id="935e6-110">Example 1: Remove a Compute Quota</span></span>
```powershell
PS C:\> Remove-AzsComputeQuota -Name "AComputeQuota"
```

<span data-ttu-id="935e6-111">Udana rozmowa w celu usunięcia przydziału obliczeniowego nie zwróci żadnego wyniku</span><span class="sxs-lookup"><span data-stu-id="935e6-111">A successful call to remove a compute quota will not return any output</span></span>

## <span data-ttu-id="935e6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="935e6-112">PARAMETERS</span></span>

### <span data-ttu-id="935e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="935e6-113">-DefaultProfile</span></span>
<span data-ttu-id="935e6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="935e6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="935e6-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="935e6-115">-InputObject</span></span>
<span data-ttu-id="935e6-116">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="935e6-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="935e6-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="935e6-117">-Location</span></span>
<span data-ttu-id="935e6-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="935e6-118">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="935e6-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="935e6-119">-Name</span></span>
<span data-ttu-id="935e6-120">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="935e6-120">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="935e6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="935e6-121">-PassThru</span></span>
<span data-ttu-id="935e6-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="935e6-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="935e6-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="935e6-123">-SubscriptionId</span></span>
<span data-ttu-id="935e6-124">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="935e6-124">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="935e6-125">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="935e6-125">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="935e6-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="935e6-126">-Confirm</span></span>
<span data-ttu-id="935e6-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="935e6-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="935e6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="935e6-128">-WhatIf</span></span>
<span data-ttu-id="935e6-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="935e6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="935e6-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="935e6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="935e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="935e6-131">CommonParameters</span></span>
<span data-ttu-id="935e6-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="935e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="935e6-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="935e6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="935e6-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="935e6-134">INPUTS</span></span>

### <span data-ttu-id="935e6-135">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="935e6-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="935e6-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="935e6-136">OUTPUTS</span></span>

### <span data-ttu-id="935e6-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="935e6-137">System.Boolean</span></span>



## <span data-ttu-id="935e6-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="935e6-138">NOTES</span></span>

<span data-ttu-id="935e6-139">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="935e6-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="935e6-140">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="935e6-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="935e6-141">INPUTobject <IComputeAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="935e6-141">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="935e6-142">`[DiskId <String>]`: Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="935e6-142">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="935e6-143">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="935e6-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="935e6-144">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="935e6-144">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="935e6-145">`[MigrationId <String>]`: Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="935e6-145">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="935e6-146">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="935e6-146">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="935e6-147">`[Publisher <String>]`: Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="935e6-147">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="935e6-148">`[QuotaName <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="935e6-148">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="935e6-149">`[Sku <String>]`: Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="935e6-149">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="935e6-150">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="935e6-150">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="935e6-151">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="935e6-151">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="935e6-152">`[Type <String>]`: Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="935e6-152">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="935e6-153">`[Version <String>]`: Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="935e6-153">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="935e6-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="935e6-154">RELATED LINKS</span></span>

