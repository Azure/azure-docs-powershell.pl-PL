---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/remove-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: ae4fc80c54aedf7f35ebfc6c0c5f16bb2e5028ee
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055693"
---
# <span data-ttu-id="37e04-101">Remove-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="37e04-101">Remove-AzsPlatformImage</span></span>

## <span data-ttu-id="37e04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37e04-102">SYNOPSIS</span></span>
<span data-ttu-id="37e04-103">Usuwanie obrazu platformy</span><span class="sxs-lookup"><span data-stu-id="37e04-103">Delete a platform image</span></span>

## <span data-ttu-id="37e04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37e04-104">SYNTAX</span></span>

### <span data-ttu-id="37e04-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="37e04-105">Delete (Default)</span></span>
```
Remove-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="37e04-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="37e04-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="37e04-107">Opis</span><span class="sxs-lookup"><span data-stu-id="37e04-107">DESCRIPTION</span></span>
<span data-ttu-id="37e04-108">Usuwanie obrazu platformy</span><span class="sxs-lookup"><span data-stu-id="37e04-108">Delete a platform image</span></span>

## <span data-ttu-id="37e04-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37e04-109">EXAMPLES</span></span>

### <span data-ttu-id="37e04-110">Przykład 1: Usuwanie obrazu platformy</span><span class="sxs-lookup"><span data-stu-id="37e04-110">Example 1: Remove a Platform Image</span></span>
```powershell
PS C:\>Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.0.0
```

<span data-ttu-id="37e04-111">Udane połączenie w celu usunięcia obrazu platformy nie zwróci żadnego wyniku</span><span class="sxs-lookup"><span data-stu-id="37e04-111">A successful call to remove a platform image will not return any output</span></span>

### <span data-ttu-id="37e04-112">Przykład 2: Usuwanie obrazu platformy nie istnieje</span><span class="sxs-lookup"><span data-stu-id="37e04-112">Example 2: Remove a Platform Image the Does Not Exist</span></span>
```powershell
PS C:\>  Remove-AzsPlatformImage -Location northwest -Offer UbuntuServer -Publisher Microsoft -Sku 16.04-LTS -Version 1.1.6

```

<span data-ttu-id="37e04-113">Udane połączenie w celu usunięcia obrazu platformy, który nie istnieje, nie powoduje zwrócenia żadnych danych wyjściowych</span><span class="sxs-lookup"><span data-stu-id="37e04-113">A successful call to remove a platform image that doesn't exist will not return any output</span></span>

## <span data-ttu-id="37e04-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37e04-114">PARAMETERS</span></span>

### <span data-ttu-id="37e04-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e04-115">-DefaultProfile</span></span>
<span data-ttu-id="37e04-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37e04-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37e04-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="37e04-117">-InputObject</span></span>
<span data-ttu-id="37e04-118">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="37e04-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="37e04-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="37e04-119">-Location</span></span>
<span data-ttu-id="37e04-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="37e04-120">Location of the resource.</span></span>

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

### <span data-ttu-id="37e04-121">-Offer</span><span class="sxs-lookup"><span data-stu-id="37e04-121">-Offer</span></span>
<span data-ttu-id="37e04-122">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="37e04-122">Name of the offer.</span></span>

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

### <span data-ttu-id="37e04-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37e04-123">-PassThru</span></span>
<span data-ttu-id="37e04-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="37e04-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="37e04-125">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="37e04-125">-Publisher</span></span>
<span data-ttu-id="37e04-126">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="37e04-126">Name of the publisher.</span></span>

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

### <span data-ttu-id="37e04-127">-SKU</span><span class="sxs-lookup"><span data-stu-id="37e04-127">-Sku</span></span>
<span data-ttu-id="37e04-128">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="37e04-128">Name of the SKU.</span></span>

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

### <span data-ttu-id="37e04-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="37e04-129">-SubscriptionId</span></span>
<span data-ttu-id="37e04-130">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="37e04-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="37e04-131">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="37e04-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="37e04-132">-Version</span><span class="sxs-lookup"><span data-stu-id="37e04-132">-Version</span></span>
<span data-ttu-id="37e04-133">Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="37e04-133">The version of the resource.</span></span>

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

### <span data-ttu-id="37e04-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37e04-134">-Confirm</span></span>
<span data-ttu-id="37e04-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37e04-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37e04-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37e04-136">-WhatIf</span></span>
<span data-ttu-id="37e04-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37e04-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37e04-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="37e04-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37e04-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e04-139">CommonParameters</span></span>
<span data-ttu-id="37e04-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e04-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e04-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37e04-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e04-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37e04-142">INPUTS</span></span>

### <span data-ttu-id="37e04-143">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="37e04-143">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="37e04-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37e04-144">OUTPUTS</span></span>

### <span data-ttu-id="37e04-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37e04-145">System.Boolean</span></span>



## <span data-ttu-id="37e04-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37e04-146">NOTES</span></span>

<span data-ttu-id="37e04-147">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="37e04-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="37e04-148">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="37e04-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="37e04-149">INPUTobject <IComputeAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="37e04-149">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="37e04-150">`[DiskId <String>]`: Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="37e04-150">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="37e04-151">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="37e04-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="37e04-152">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="37e04-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="37e04-153">`[MigrationId <String>]`: Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="37e04-153">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="37e04-154">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="37e04-154">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="37e04-155">`[Publisher <String>]`: Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="37e04-155">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="37e04-156">`[QuotaName <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="37e04-156">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="37e04-157">`[Sku <String>]`: Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="37e04-157">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="37e04-158">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="37e04-158">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="37e04-159">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="37e04-159">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="37e04-160">`[Type <String>]`: Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="37e04-160">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="37e04-161">`[Version <String>]`: Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="37e04-161">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="37e04-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37e04-162">RELATED LINKS</span></span>

