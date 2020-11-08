---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/get-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: 5523dd35ae91b9fea7db5f2451401793cb6059c2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055919"
---
# <span data-ttu-id="cff80-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="cff80-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="cff80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cff80-102">SYNOPSIS</span></span>
<span data-ttu-id="cff80-103">Uzyskiwanie określonego elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="cff80-103">Get a specific gallery item.</span></span>

## <span data-ttu-id="cff80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cff80-104">SYNTAX</span></span>

### <span data-ttu-id="cff80-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="cff80-105">List (Default)</span></span>
```
Get-AzsGalleryItem [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cff80-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="cff80-106">Get</span></span>
```
Get-AzsGalleryItem -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="cff80-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cff80-107">GetViaIdentity</span></span>
```
Get-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="cff80-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cff80-108">DESCRIPTION</span></span>
<span data-ttu-id="cff80-109">Uzyskiwanie określonego elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="cff80-109">Get a specific gallery item.</span></span>

## <span data-ttu-id="cff80-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cff80-110">EXAMPLES</span></span>

### <span data-ttu-id="cff80-111">Przykład 1: Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="cff80-111">Example 1: Get-AzsGalleryItem</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM
```

<span data-ttu-id="cff80-112">Pobiera element galerii według nazwy.</span><span class="sxs-lookup"><span data-stu-id="cff80-112">Gets the gallery item by name.</span></span>

### <span data-ttu-id="cff80-113">Przykład 2: elementy galerii list</span><span class="sxs-lookup"><span data-stu-id="cff80-113">Example 2: List Gallery Items</span></span>
```powershell
PS C:\> Get-AzsGalleryItem

Name                                       Publisher PublisherDisplayName  ItemName                  ItemDisplayName
----                                       --------- --------------------  --------                  ---------------
Canonical.UbuntuServer1804LTS-ARM.1.0.3    Canonical Canonical             UbuntuServer1804LTS-ARM   Ubuntu Server 1...
Microsoft.AddOnRP-WindowsServer.1.1910.3   Microsoft Microsoft             AddOnRP-WindowsServer     Microsoft Azure...
Microsoft.AdminOffer.6.0.0                 Microsoft Microsoft Corporation AdminOffer                Offer
Microsoft.AvailabilitySet-ARM.1.0.1        Microsoft Microsoft             AvailabilitySet-ARM       Availability Set
Microsoft.Connection-ARM.1.2.2             Microsoft Microsoft             Connection-ARM            Connection
Microsoft.CustomScriptExtension-arm.2.0.10 Microsoft Microsoft Corp.       CustomScriptExtension-arm Custom Script E...
Microsoft.DSC-arm.2.0.7                    Microsoft Microsoft Corp.       DSC-arm                   PowerShell Desi...
Microsoft.DnsZone-ARM.1.0.1                Microsoft Microsoft             DnsZone-ARM               DNS zone
Microsoft.Image-ARM.1.0.2                  Microsoft Microsoft             Image-ARM                 Image
Microsoft.KeyVault.1.0.14                  Microsoft Microsoft             KeyVault                  Key Vault
Microsoft.LoadBalancer-ARM.1.0.2           Microsoft Microsoft             LoadBalancer-ARM          Load Balancer
Microsoft.LocalNetworkGateway-ARM.1.0.3    Microsoft Microsoft             LocalNetworkGateway-ARM   Local network g...
Microsoft.ManagedDisk-ARM.1.0.2            Microsoft Microsoft             ManagedDisk-ARM           Managed Disks
Microsoft.NetworkInterface-ARM.1.0.4       Microsoft Microsoft             NetworkInterface-ARM      Network interface
Microsoft.NetworkSecurityGroup-ARM.1.0.4   Microsoft Microsoft             NetworkSecurityGroup-ARM  Network securit...
Microsoft.Offer.6.0.0                      Microsoft Microsoft Corporation Offer                     Offer
Microsoft.Plan.6.0.0                       Microsoft Microsoft Corporation Plan                      Plan
Microsoft.PublicIPAddress-ARM.1.0.2        Microsoft Microsoft             PublicIPAddress-ARM       Public IP address
Microsoft.PublicIPPool-ARM.1.0.0           Microsoft Microsoft             PublicIPPool-ARM          Public IP pool
Microsoft.ResourceGroup.6.0.0              Microsoft Microsoft             ResourceGroup             Resource group
Microsoft.RouteTable-ARM.1.0.2             Microsoft Microsoft             RouteTable-ARM            Route table
Microsoft.ScaleUnitNode-ARM.1.0.0          Microsoft Microsoft             ScaleUnitNode-ARM         Scale Unit Node
Microsoft.Snapshot-ARM.1.0.2               Microsoft Microsoft             Snapshot-ARM              Snapshot
Microsoft.StorageAccount-ARM.101.0.1       Microsoft Microsoft             StorageAccount-ARM        Storage account
Microsoft.StorageAccount-ARM.1.0.3         Microsoft Microsoft             StorageAccount-ARM        Storage account...
Microsoft.Template.6.0.0                   Microsoft Microsoft             Template                  Template deploy...
Microsoft.TenantSubscription.6.0.0         Microsoft Microsoft Corporation TenantSubscription        Subscription
Microsoft.VirtualMachine-ARM.1.0.2         Microsoft Microsoft             VirtualMachine-ARM        Virtual machine
Microsoft.VirtualNetwork-ARM.1.0.4         Microsoft Microsoft             VirtualNetwork-ARM        Virtual network
Microsoft.VirtualNetworkGateway-ARM.1.0.3  Microsoft Microsoft             VirtualNetworkGateway-ARM Virtual network...
microsoft.antimalware-windows-arm.1.0.0    microsoft Microsoft Corp.       antimalware-windows-arm   Microsoft Antim...
microsoft.custom-script2-linux-arm.3.0.0   microsoft Microsoft Corp.       custom-script2-linux-arm  Custom Script F...
microsoft.custom-script-linux-arm.2.0.50   microsoft Microsoft Corp.       custom-script-linux-arm   Custom Script F...
microsoft.docker-arm.1.1.0                 microsoft Microsoft             docker-arm                Docker
microsoft.vmss.7.1.7                       microsoft Microsoft             vmss                      Virtual machine...

```

<span data-ttu-id="cff80-114">Zawiera listę wszystkich elementów dostępnych w galerii stosów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cff80-114">Lists all the items available in the Azure Stack gallery.</span></span>

## <span data-ttu-id="cff80-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cff80-115">PARAMETERS</span></span>

### <span data-ttu-id="cff80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff80-116">-DefaultProfile</span></span>
<span data-ttu-id="cff80-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cff80-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cff80-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cff80-118">-InputObject</span></span>
<span data-ttu-id="cff80-119">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="cff80-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cff80-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cff80-120">-Name</span></span>
<span data-ttu-id="cff80-121">Tożsamość elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="cff80-121">Identity of the gallery item.</span></span>
<span data-ttu-id="cff80-122">Zawiera nazwę wydawcy, nazwę elementu i może zawierać wersję rozdzieloną znakiem kropki.</span><span class="sxs-lookup"><span data-stu-id="cff80-122">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cff80-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cff80-123">-PassThru</span></span>
<span data-ttu-id="cff80-124">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="cff80-124">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cff80-125">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="cff80-125">-SubscriptionId</span></span>
<span data-ttu-id="cff80-126">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cff80-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cff80-127">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="cff80-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cff80-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff80-128">CommonParameters</span></span>
<span data-ttu-id="cff80-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cff80-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff80-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cff80-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff80-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cff80-131">INPUTS</span></span>

### <span data-ttu-id="cff80-132">Microsoft. Azure. PowerShell. polecenia cmdlet. Gallery. modele. IGalleryIdentity</span><span class="sxs-lookup"><span data-stu-id="cff80-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="cff80-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cff80-133">OUTPUTS</span></span>

### <span data-ttu-id="cff80-134">Microsoft. Azure. PowerShell. polecenia cmdlet. Gallery. models. Api20150401. IGalleryItem</span><span class="sxs-lookup"><span data-stu-id="cff80-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="cff80-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cff80-135">NOTES</span></span>

<span data-ttu-id="cff80-136">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cff80-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cff80-137">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cff80-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cff80-138">INPUTobject <IGalleryIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="cff80-138">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cff80-139">`[GalleryItemName <String>]`: Tożsamość elementu galerii.</span><span class="sxs-lookup"><span data-stu-id="cff80-139">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="cff80-140">Zawiera nazwę wydawcy, nazwę elementu i może zawierać wersję rozdzieloną znakiem kropki.</span><span class="sxs-lookup"><span data-stu-id="cff80-140">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="cff80-141">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cff80-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cff80-142">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cff80-142">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cff80-143">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="cff80-143">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="cff80-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cff80-144">RELATED LINKS</span></span>

