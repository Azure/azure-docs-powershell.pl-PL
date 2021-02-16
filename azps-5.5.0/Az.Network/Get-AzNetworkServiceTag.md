---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkservicetag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkServiceTag.md
ms.openlocfilehash: c511dc6eba981708557797dc657e4626621f9131
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203075"
---
# <span data-ttu-id="52f4b-101">Get-AzNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="52f4b-101">Get-AzNetworkServiceTag</span></span>

## <span data-ttu-id="52f4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52f4b-102">SYNOPSIS</span></span>
<span data-ttu-id="52f4b-103">Pobiera listę zasobów informacji o tagach usługi.</span><span class="sxs-lookup"><span data-stu-id="52f4b-103">Gets the list of service tag information resources.</span></span>

## <span data-ttu-id="52f4b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="52f4b-104">SYNTAX</span></span>

```
Get-AzNetworkServiceTag -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52f4b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="52f4b-105">DESCRIPTION</span></span>
<span data-ttu-id="52f4b-106">Polecenie **cmdlet Get-AzNetworkServiceTag** pobiera listę zasobów informacji o tagu usługi.</span><span class="sxs-lookup"><span data-stu-id="52f4b-106">The **Get-AzNetworkServiceTag** cmdlet gets the list of service tag information resources.</span></span>

<span data-ttu-id="52f4b-107">Należy pamiętać, że podane informacje o regionie platformy Azure będą używane jako odwołanie do wersji (nie jako filtr na podstawie lokalizacji).</span><span class="sxs-lookup"><span data-stu-id="52f4b-107">Please note that the Azure region information you specify will be used as a reference for version (not as a filter based on location).</span></span> <span data-ttu-id="52f4b-108">Na przykład nawet jeśli określisz, że będziesz mieć listę tagów usługi ze szczegółami prefiksu we wszystkich regionach, ale ograniczonych do chmury, do której należy Twoja subskrypcja (np. publiczna, rząd Stanów Zjednoczonych, Chiny lub `-Location eastus2` Niemcy).</span><span class="sxs-lookup"><span data-stu-id="52f4b-108">For example, even if you specify `-Location eastus2` you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to (i.e. Public, US government, China or Germany).</span></span>

## <span data-ttu-id="52f4b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="52f4b-109">EXAMPLES</span></span>

### <span data-ttu-id="52f4b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="52f4b-110">Example 1</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags

Name         : Public
Id           : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxx/providers/Microsoft.Network/serviceTags/Public
Type         : Microsoft.Network/serviceTags
ChangeNumber : 63
Cloud        : Public
Values       : {ApiManagement, ApiManagement.AustraliaCentral, ApiManagement.AustraliaCentral2, ApiManagement.AustraliaEast...}

PS C:\> $serviceTags.Values

Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : ApiManagement.AustraliaCentral
System Service   : AzureApiManagement
Region           : australiacentral
Address Prefixes : {20.36.106.68/31, 20.36.107.176/28}
Change Number    : 2

Name             : ApiManagement.AustraliaCentral2
System Service   : AzureApiManagement
Region           : australiacentral2
Address Prefixes : {20.36.114.20/31, 20.36.115.128/28}
Change Number    : 2

Name             : ApiManagement.AustraliaEast
System Service   : AzureApiManagement
Region           : australiaeast
Address Prefixes : {13.70.72.28/31, 13.70.72.240/28, 13.75.217.184/32, 13.75.221.78/32...}
Change Number    : 3

Name             : ApiManagement.AustraliaSoutheast
System Service   : AzureApiManagement
Region           : australiasoutheast
Address Prefixes : {13.77.50.68/31, 13.77.52.224/28}
Change Number    : 2

...
```

<span data-ttu-id="52f4b-111">Polecenie pobiera listę zasobów informacji o tagu usługi i przechowuje je w `serviceTags` zmiennej.</span><span class="sxs-lookup"><span data-stu-id="52f4b-111">The command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>

### <span data-ttu-id="52f4b-112">Przykład 2. Uzyskiwanie wszystkich prefiksów adresów dla usługi AzureSQL</span><span class="sxs-lookup"><span data-stu-id="52f4b-112">Example 2: Get all address prefixes for AzureSQL</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $sql = $serviceTags.Values | Where-Object { $_.Name -eq "Sql" }
PS C:\> $sql

Name             : Sql
System Service   : AzureSQL
Address Prefixes : {13.65.31.249/32, 13.65.39.207/32, 13.65.85.183/32, 13.65.200.105/32...}
Change Number    : 18

PS C:\> $sql.Properties.AddressPrefixes.Count
644
PS C:\> $sql.Properties.AddressPrefixes
13.65.31.249/32
13.65.39.207/32
13.65.85.183/32
13.65.200.105/32
13.65.209.243/32
...
```

<span data-ttu-id="52f4b-113">Pierwsze polecenie pobiera listę zasobów informacji o tagu usługi i przechowuje je w `serviceTags` zmiennej.</span><span class="sxs-lookup"><span data-stu-id="52f4b-113">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="52f4b-114">Drugie polecenie filtruje listę w celu wybrania zasobu informacyjnego dla języka Sql.</span><span class="sxs-lookup"><span data-stu-id="52f4b-114">The second command filters the list to select information resource for Sql.</span></span>

### <span data-ttu-id="52f4b-115">Przykład 3. Uzyskiwanie zasobu informacji o tagu usługi magazynu dla Stanów Zjednoczonych Zachód 2</span><span class="sxs-lookup"><span data-stu-id="52f4b-115">Example 3: Get Storage's service tag information resource for West US 2</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { $_.Name -eq "Storage.WestUS2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Name -like "Storage*" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5

PS C:\> $serviceTags.Values | Where-Object { $_.Properties.SystemService -eq "AzureStorage" -and $_.Properties.Region -eq "westus2" }

Name             : Storage.WestUS2
System Service   : AzureStorage
Region           : westus2
Address Prefixes : {13.66.176.16/28, 13.66.176.48/28, 13.66.232.64/28, 13.66.232.208/28...}
Change Number    : 5
```

<span data-ttu-id="52f4b-116">Pierwsze polecenie pobiera listę zasobów informacji o tagu usługi i przechowuje je w `serviceTags` zmiennej.</span><span class="sxs-lookup"><span data-stu-id="52f4b-116">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="52f4b-117">Poniższe polecenia pokazują różne sposoby filtrowania listy w celu wybrania informacji o tagu usługi dla magazynu w Zachód Stanów Zjednoczonych 2.</span><span class="sxs-lookup"><span data-stu-id="52f4b-117">The following commands show various way to filter the list to select service tag information for Storage in West US 2.</span></span>

### <span data-ttu-id="52f4b-118">Przykład 4. Uzyskiwanie wszystkich globalnych zasobów z informacjami o tagach usług</span><span class="sxs-lookup"><span data-stu-id="52f4b-118">Example 4: Get all global service tag information resources</span></span>
```powershell
PS C:\> $serviceTags = Get-AzNetworkServiceTag -Location eastus2
PS C:\> $serviceTags.Values | Where-Object { -not $_.Properties.Region }


Name             : ApiManagement
System Service   : AzureApiManagement
Address Prefixes : {13.64.39.16/32, 13.66.138.92/31, 13.66.140.176/28, 13.67.8.108/31...}
Change Number    : 7

Name             : AppService
System Service   : AzureAppService
Address Prefixes : {13.64.73.110/32, 13.65.30.245/32, 13.65.37.122/32, 13.65.39.165/32...}
Change Number    : 13

Name             : AppServiceManagement
System Service   : AzureAppServiceManagement
Address Prefixes : {13.64.115.203/32, 13.66.140.0/26, 13.67.8.128/26, 13.69.64.128/26...}
Change Number    : 7

Name             : AzureActiveDirectory
System Service   : AzureAD
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.67.50.224/29...}
Change Number    : 3

Name             : AzureActiveDirectoryDomainServices
System Service   : AzureIdentity
Address Prefixes : {13.64.151.161/32, 13.66.141.64/27, 13.67.9.224/27, 13.69.66.160/27...}
Change Number    : 2

...
```

<span data-ttu-id="52f4b-119">Pierwsze polecenie pobiera listę zasobów informacji o tagu usługi i przechowuje je w `serviceTags` zmiennej.</span><span class="sxs-lookup"><span data-stu-id="52f4b-119">The first command gets the list of service tag information resources and stores it in variable `serviceTags`.</span></span>
<span data-ttu-id="52f4b-120">Drugie polecenie filtruje listę w celu wybrania tylko tych, dla których nie ustawiono regionu.</span><span class="sxs-lookup"><span data-stu-id="52f4b-120">The second command filters the list to select only those without set region.</span></span>

## <span data-ttu-id="52f4b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52f4b-121">PARAMETERS</span></span>

### <span data-ttu-id="52f4b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f4b-122">-DefaultProfile</span></span>
<span data-ttu-id="52f4b-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="52f4b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52f4b-124">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="52f4b-124">-Location</span></span>
<span data-ttu-id="52f4b-125">Lokalizacja, która będzie używana jako odwołanie do wersji (nie jako filtr oparty na lokalizacji, zostanie wyświetlona lista tagów usługi ze szczegółami prefiksu we wszystkich regionach, ale ograniczona do chmury, do której należy Twoja subskrypcja).</span><span class="sxs-lookup"><span data-stu-id="52f4b-125">The location that will be used as a reference for version (not as a filter based on location, you will get the list of service tags with prefix details across all regions but limited to the cloud that your subscription belongs to).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52f4b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f4b-126">CommonParameters</span></span>
<span data-ttu-id="52f4b-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f4b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f4b-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52f4b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f4b-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52f4b-129">INPUTS</span></span>

### <span data-ttu-id="52f4b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="52f4b-130">System.String</span></span>

## <span data-ttu-id="52f4b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="52f4b-131">OUTPUTS</span></span>

### <span data-ttu-id="52f4b-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span><span class="sxs-lookup"><span data-stu-id="52f4b-132">Microsoft.Azure.Commands.Network.Models.PSNetworkServiceTag</span></span>

## <span data-ttu-id="52f4b-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="52f4b-133">NOTES</span></span>

## <span data-ttu-id="52f4b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52f4b-134">RELATED LINKS</span></span>
