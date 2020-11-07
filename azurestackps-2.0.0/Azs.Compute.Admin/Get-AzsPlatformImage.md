---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: d91e930c486fea5c7a17e5a8f7d8f8d30a88b351
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93894030"
---
# <span data-ttu-id="cace5-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="cace5-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="cace5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cace5-102">SYNOPSIS</span></span>
<span data-ttu-id="cace5-103">Zwraca określony przez program Publisher, ofertę, jednostki SKU i wersję odpowiedniego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="cace5-103">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="cace5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cace5-104">SYNTAX</span></span>

### <span data-ttu-id="cace5-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="cace5-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="cace5-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="cace5-106">Get</span></span>
```
Get-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cace5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cace5-107">GetViaIdentity</span></span>
```
Get-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cace5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cace5-108">DESCRIPTION</span></span>
<span data-ttu-id="cace5-109">Zwraca określony przez program Publisher, ofertę, jednostki SKU i wersję odpowiedniego obrazu platformy.</span><span class="sxs-lookup"><span data-stu-id="cace5-109">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="cace5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cace5-110">EXAMPLES</span></span>

### <span data-ttu-id="cace5-111">Przykład 1: pobieranie wszystkich platform obrazy</span><span class="sxs-lookup"><span data-stu-id="cace5-111">Example 1: Get All Platform Images</span></span>
```powershell
PS C:\> Get-AzsPlatformImage

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/loc
                    al/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=r
                    wdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="cace5-112">Aby uzyskać listę wszystkich obrazów na platformie, należy pozostawić wszystkie parametry puste.</span><span class="sxs-lookup"><span data-stu-id="cace5-112">Get a list of all Platform Images by leaving all parameters blank.</span></span>

### <span data-ttu-id="cace5-113">Przykład 2: uzyskiwanie określonego obrazu platformy</span><span class="sxs-lookup"><span data-stu-id="cace5-113">Example 2: Get Specific Platform Image</span></span>
```powershell
PS C:\> Get-AzsPlatformImage -Offer ExampleOffer -Publisher ExamplePublisher -Location local -Sku ExampleSku -Version 1.0.0

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifa
                    ctTypes/platformImage/publishers/ExamplePublisher/offers/ExampleOffer/skus/ExampleSku/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&s
                    e=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="cace5-114">Określ ofertę, wydawcę, lokalizację, jednostkę SKU i wersję, aby pobrać obraz platformy.</span><span class="sxs-lookup"><span data-stu-id="cace5-114">Specify the Offer, Publisher, Location, Sku, and Version to retrieve a Platform Image.</span></span>

## <span data-ttu-id="cace5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cace5-115">PARAMETERS</span></span>

### <span data-ttu-id="cace5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cace5-116">-DefaultProfile</span></span>
<span data-ttu-id="cace5-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cace5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cace5-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cace5-118">-InputObject</span></span>
<span data-ttu-id="cace5-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="cace5-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cace5-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cace5-120">-Location</span></span>
<span data-ttu-id="cace5-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="cace5-121">Location of the resource.</span></span>

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

### <span data-ttu-id="cace5-122">-Offer</span><span class="sxs-lookup"><span data-stu-id="cace5-122">-Offer</span></span>
<span data-ttu-id="cace5-123">Imię i nazwisko oferty.</span><span class="sxs-lookup"><span data-stu-id="cace5-123">Name of the offer.</span></span>

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

### <span data-ttu-id="cace5-124">— Wydawca</span><span class="sxs-lookup"><span data-stu-id="cace5-124">-Publisher</span></span>
<span data-ttu-id="cace5-125">Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="cace5-125">Name of the publisher.</span></span>

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

### <span data-ttu-id="cace5-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="cace5-126">-Sku</span></span>
<span data-ttu-id="cace5-127">Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="cace5-127">Name of the SKU.</span></span>

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

### <span data-ttu-id="cace5-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="cace5-128">-SubscriptionId</span></span>
<span data-ttu-id="cace5-129">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cace5-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cace5-130">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="cace5-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cace5-131">-Version</span><span class="sxs-lookup"><span data-stu-id="cace5-131">-Version</span></span>
<span data-ttu-id="cace5-132">Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="cace5-132">The version of the resource.</span></span>

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

### <span data-ttu-id="cace5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cace5-133">CommonParameters</span></span>
<span data-ttu-id="cace5-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cace5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cace5-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cace5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cace5-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cace5-136">INPUTS</span></span>

### <span data-ttu-id="cace5-137">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cace5-137">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="cace5-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cace5-138">OUTPUTS</span></span>

### <span data-ttu-id="cace5-139">Microsoft. Azure. PowerShell. polecenia. ComputeAdmin. models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="cace5-139">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="cace5-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cace5-140">NOTES</span></span>

<span data-ttu-id="cace5-141">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cace5-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cace5-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cace5-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cace5-143">INPUTobject <IComputeAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="cace5-143">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cace5-144">`[DiskId <String>]`: Identyfikator GUID dysku jako tożsamość.</span><span class="sxs-lookup"><span data-stu-id="cace5-144">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="cace5-145">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cace5-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cace5-146">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="cace5-146">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cace5-147">`[MigrationId <String>]`: Nazwa GUID zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="cace5-147">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="cace5-148">`[Offer <String>]`: Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="cace5-148">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="cace5-149">`[Publisher <String>]`: Nazwa wydawcy.</span><span class="sxs-lookup"><span data-stu-id="cace5-149">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="cace5-150">`[QuotaName <String>]`: Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="cace5-150">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="cace5-151">`[Sku <String>]`: Nazwa jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="cace5-151">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="cace5-152">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cace5-152">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cace5-153">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="cace5-153">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cace5-154">`[Type <String>]`: Typ rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="cace5-154">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="cace5-155">`[Version <String>]`: Wersja zasobu.</span><span class="sxs-lookup"><span data-stu-id="cace5-155">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="cace5-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cace5-156">RELATED LINKS</span></span>

