---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsvmextension
schema: 2.0.0
ms.openlocfilehash: 0b2bca9555b14a391df69acc4abdb2fc8c95017c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055691"
---
# <span data-ttu-id="196d5-101">Remove-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="196d5-101">Remove-AzsVMExtension</span></span>

## <span data-ttu-id="196d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="196d5-102">SYNOPSIS</span></span>
<span data-ttu-id="196d5-103">Umożliwia usunięcie określonego obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="196d5-103">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="196d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="196d5-104">SYNTAX</span></span>

### <span data-ttu-id="196d5-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="196d5-105">Delete (Default)</span></span>
```
Remove-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="196d5-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="196d5-106">DeleteViaIdentity</span></span>
```
Remove-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="196d5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="196d5-107">DESCRIPTION</span></span>
<span data-ttu-id="196d5-108">Umożliwia usunięcie określonego obrazu rozszerzenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="196d5-108">Deletes specified Virtual Machine Extension Image.</span></span>

## <span data-ttu-id="196d5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="196d5-109">EXAMPLES</span></span>

### <span data-ttu-id="196d5-110">Przykład 1. Usuń istniejące rozszerzenie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="196d5-110">Example 1: Remove a VM Extension that Exists</span></span> 
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type MicroExtension -Version 0.1.0
```

<span data-ttu-id="196d5-111">Udana rozmowa w celu usunięcia przydziału obliczeniowego nie zwróci żadnego wyniku</span><span class="sxs-lookup"><span data-stu-id="196d5-111">A successful call to remove a compute quota will not return any output</span></span>

### <span data-ttu-id="196d5-112">Przykład 2: Usuwanie rozszerzenia maszyny wirtualnej, które nie istnieje</span><span class="sxs-lookup"><span data-stu-id="196d5-112">Example 2: Remove a VM Extension that Does Not Exist</span></span>
```powershell
PS C:\> Remove-AzsVMExtension -Location local -Publisher Microsoft -Type DoesntExist -Version 9.8.7
```

<span data-ttu-id="196d5-113">Udane połączenie w celu usunięcia obrazu platformy, który nie istnieje, nie powoduje zwrócenia żadnych danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="196d5-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="196d5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="196d5-114">PARAMETERS</span></span>

### <span data-ttu-id="196d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="196d5-115">-DefaultProfile</span></span>
<span data-ttu-id="196d5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="196d5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="196d5-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="196d5-117">-InputObject</span></span>
<span data-ttu-id="196d5-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="196d5-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="196d5-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="196d5-119">-Location</span></span>
<span data-ttu-id="196d5-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="196d5-120">Location of the resource.</span></span>

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

### <span data-ttu-id="196d5-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="196d5-121">-PassThru</span></span>
<span data-ttu-id="196d5-122">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="196d5-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="196d5-123">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="196d5-123">-Publisher</span></span>
<span data-ttu-id="196d5-124">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="196d5-124">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="196d5-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="196d5-125">-SubscriptionId</span></span>
<span data-ttu-id="196d5-126">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="196d5-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="196d5-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="196d5-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="196d5-128">-Type</span><span class="sxs-lookup"><span data-stu-id="196d5-128">-Type</span></span>
<span data-ttu-id="196d5-129">Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="196d5-129">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="196d5-130">-Version</span><span class="sxs-lookup"><span data-stu-id="196d5-130">-Version</span></span>
<span data-ttu-id="196d5-131">Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="196d5-131">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="196d5-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="196d5-132">-Confirm</span></span>
<span data-ttu-id="196d5-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="196d5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="196d5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="196d5-134">-WhatIf</span></span>
<span data-ttu-id="196d5-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="196d5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="196d5-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="196d5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="196d5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="196d5-137">CommonParameters</span></span>
<span data-ttu-id="196d5-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="196d5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="196d5-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="196d5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="196d5-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="196d5-140">INPUTS</span></span>

### <span data-ttu-id="196d5-141">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="196d5-141">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="196d5-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="196d5-142">OUTPUTS</span></span>

### <span data-ttu-id="196d5-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="196d5-143">System.Boolean</span></span>



## <span data-ttu-id="196d5-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="196d5-144">NOTES</span></span>

<span data-ttu-id="196d5-145">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="196d5-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="196d5-146">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="196d5-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="196d5-147">INPUTobject <IComputeAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="196d5-147">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="196d5-148">`[DiskId <String>]`: Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="196d5-148">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="196d5-149">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="196d5-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="196d5-150">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="196d5-150">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="196d5-151">`[MigrationId <String>]`: Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="196d5-151">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="196d5-152">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="196d5-152">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="196d5-153">`[Publisher <String>]`: Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="196d5-153">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="196d5-154">`[QuotaName <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="196d5-154">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="196d5-155">`[Sku <String>]`: Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="196d5-155">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="196d5-156">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="196d5-156">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="196d5-157">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="196d5-157">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="196d5-158">`[Type <String>]`: Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="196d5-158">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="196d5-159">`[Version <String>]`: Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="196d5-159">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="196d5-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="196d5-160">RELATED LINKS</span></span>

