---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzVpnClientRevokedCertificate.md
ms.openlocfilehash: f9dbdaf531f4ccc35543dc542dc0637b9795360e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890394"
---
# <span data-ttu-id="66474-101">New-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="66474-101">New-AzVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="66474-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66474-102">SYNOPSIS</span></span>
<span data-ttu-id="66474-103">Tworzy nowy certyfikat odwołania klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="66474-103">Creates a new VPN client-revocation certificate.</span></span>

## <span data-ttu-id="66474-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66474-104">SYNTAX</span></span>

```
New-AzVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66474-105">Opis</span><span class="sxs-lookup"><span data-stu-id="66474-105">DESCRIPTION</span></span>
<span data-ttu-id="66474-106">Polecenie cmdlet **New-AzVpnClientRevokedCertificate** tworzy nowy certyfikat odwołania klienta wirtualnej sieci prywatnej (VPN) do użycia w wirtualnej bramie sieci.</span><span class="sxs-lookup"><span data-stu-id="66474-106">The **New-AzVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="66474-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="66474-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>

<span data-ttu-id="66474-108">To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="66474-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="66474-109">Zamiast tego certyfikat utworzony za pomocą polecenia **New-AzVpnClientRevokedCertificate** jest wykorzystywany w połączeniu z poleceniem cmdlet New-AzVirtualNetworkGateway podczas tworzenia nowej bramy.</span><span class="sxs-lookup"><span data-stu-id="66474-109">Instead, the certificate created by **New-AzVpnClientRevokedCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="66474-110">Załóżmy na przykład, że tworzysz nowy certyfikat i zapisujesz go w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="66474-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="66474-111">Po utworzeniu nowej bramy wirtualnej można użyć tego obiektu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="66474-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="66474-112">Na przykład</span><span class="sxs-lookup"><span data-stu-id="66474-112">For instance,</span></span>

`New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

<span data-ttu-id="66474-113">Aby uzyskać więcej informacji, zobacz dokumentację New-AzVirtualNetworkGateway polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66474-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="66474-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66474-114">EXAMPLES</span></span>

### <span data-ttu-id="66474-115">Przykład 1. Tworzenie nowego certyfikatu odwołanego przez klienta</span><span class="sxs-lookup"><span data-stu-id="66474-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="66474-116">To polecenie tworzy nowy certyfikat odwołany przez klienta i zapisuje obiekt Certificate w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="66474-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="66474-117">Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzVirtualNetworkGateway** , aby dodać certyfikat do nowej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="66474-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="66474-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66474-118">PARAMETERS</span></span>

### <span data-ttu-id="66474-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66474-119">-DefaultProfile</span></span>
<span data-ttu-id="66474-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="66474-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66474-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="66474-121">-Name</span></span>
<span data-ttu-id="66474-122">Określa unikatową nazwę nowego certyfikatu odwołania klienta.</span><span class="sxs-lookup"><span data-stu-id="66474-122">Specifies a unique name for the new client-revocation certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66474-123">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="66474-123">-Thumbprint</span></span>
<span data-ttu-id="66474-124">Określa unikatowy identyfikator dodawanego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="66474-124">Specifies the unique identifier of the certificate being added.</span></span>

<span data-ttu-id="66474-125">Możesz zwrócić informacje o odcisku palca dotyczące certyfikatów przy użyciu polecenia programu Windows PowerShell podobnej do następującego:</span><span class="sxs-lookup"><span data-stu-id="66474-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path Cert:\LocalMachine\Root`

<span data-ttu-id="66474-126">Powyższe polecenie zwraca informacje dotyczące wszystkich certyfikatów komputerów lokalnych znajdujących się w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="66474-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66474-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66474-127">CommonParameters</span></span>
<span data-ttu-id="66474-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66474-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66474-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66474-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66474-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66474-130">INPUTS</span></span>

###  
<span data-ttu-id="66474-131">To polecenie cmdlet nie akceptuje danych wejściowych potoku.</span><span class="sxs-lookup"><span data-stu-id="66474-131">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="66474-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66474-132">OUTPUTS</span></span>

###  
<span data-ttu-id="66474-133">To polecenie cmdlet tworzy nowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="66474-133">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="66474-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66474-134">NOTES</span></span>

## <span data-ttu-id="66474-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66474-135">RELATED LINKS</span></span>

[<span data-ttu-id="66474-136">Dodaj-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="66474-136">Add-AzVpnClientRevokedCertificate</span></span>](./Add-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="66474-137">Get-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="66474-137">Get-AzVpnClientRevokedCertificate</span></span>](./Get-AzVpnClientRevokedCertificate.md)

[<span data-ttu-id="66474-138">Remove-AzVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="66474-138">Remove-AzVpnClientRevokedCertificate</span></span>](./Remove-AzVpnClientRevokedCertificate.md)


