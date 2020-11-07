---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 973E1E53-983F-45A7-A7CF-18A8D96EC4E6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrevokedcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRevokedCertificate.md
ms.openlocfilehash: 8e4b9c5e921ce9a1b46e92b40b6877beb51dc709
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550635"
---
# <span data-ttu-id="300e4-101">New-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="300e4-101">New-AzureRmVpnClientRevokedCertificate</span></span>

## <span data-ttu-id="300e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="300e4-102">SYNOPSIS</span></span>
<span data-ttu-id="300e4-103">Tworzy nowy certyfikat odwołania klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="300e4-103">Creates a new VPN client-revocation certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="300e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="300e4-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRevokedCertificate -Name <String> -Thumbprint <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="300e4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="300e4-105">DESCRIPTION</span></span>
<span data-ttu-id="300e4-106">Polecenie cmdlet **New-AzureRmVpnClientRevokedCertificate** tworzy nowy certyfikat odwołania klienta wirtualnej sieci prywatnej (VPN) do użycia w wirtualnej bramie sieci.</span><span class="sxs-lookup"><span data-stu-id="300e4-106">The **New-AzureRmVpnClientRevokedCertificate** cmdlet creates a new virtual private network (VPN) client-revocation certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="300e4-107">Certyfikaty odwołań klienta uniemożliwiają komputerom klienckim używanie określonego certyfikatu do uwierzytelniania.</span><span class="sxs-lookup"><span data-stu-id="300e4-107">Client-revocation certificates prevent client computers from using the specified certificate for authentication.</span></span>

<span data-ttu-id="300e4-108">To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="300e4-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="300e4-109">Zamiast tego certyfikat utworzony za pomocą polecenia **New-AzureRmVpnClientRevokedCertificate** jest wykorzystywany w połączeniu z poleceniem cmdlet New-AzureRmVirtualNetworkGateway podczas tworzenia nowej bramy.</span><span class="sxs-lookup"><span data-stu-id="300e4-109">Instead, the certificate created by **New-AzureRmVpnClientRevokedCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when it creates a new gateway.</span></span>
<span data-ttu-id="300e4-110">Załóżmy na przykład, że tworzysz nowy certyfikat i zapisujesz go w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="300e4-110">For instance, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="300e4-111">Po utworzeniu nowej bramy wirtualnej można użyć tego obiektu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="300e4-111">You can then use that certificate object when you create a new virtual gateway.</span></span>
<span data-ttu-id="300e4-112">Na przykład</span><span class="sxs-lookup"><span data-stu-id="300e4-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRevokedCertificates $Certificate`

<span data-ttu-id="300e4-113">Aby uzyskać więcej informacji, zobacz dokumentację New-AzureRmVirtualNetworkGateway polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="300e4-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="300e4-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="300e4-114">EXAMPLES</span></span>

### <span data-ttu-id="300e4-115">Przykład 1. Tworzenie nowego certyfikatu odwołanego przez klienta</span><span class="sxs-lookup"><span data-stu-id="300e4-115">Example 1: Create a new client-revoked certificate</span></span>
```
PS C:\>$Certificate = New-AzureRmVpnClientRevokedCertificate -Name "ContosoClientRevokedCertificate" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="300e4-116">To polecenie tworzy nowy certyfikat odwołany przez klienta i zapisuje obiekt Certificate w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="300e4-116">This command creates a new client-revoked certificate and stores the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="300e4-117">Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzureRmVirtualNetworkGateway** , aby dodać certyfikat do nowej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="300e4-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add the certificate to a new virtual network gateway.</span></span>

## <span data-ttu-id="300e4-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="300e4-118">PARAMETERS</span></span>

### <span data-ttu-id="300e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="300e4-119">-DefaultProfile</span></span>
<span data-ttu-id="300e4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="300e4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="300e4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="300e4-121">-Name</span></span>
<span data-ttu-id="300e4-122">Określa unikatową nazwę nowego certyfikatu odwołania klienta.</span><span class="sxs-lookup"><span data-stu-id="300e4-122">Specifies a unique name for the new client-revocation certificate.</span></span>

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

### <span data-ttu-id="300e4-123">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="300e4-123">-Thumbprint</span></span>
<span data-ttu-id="300e4-124">Określa unikatowy identyfikator dodawanego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="300e4-124">Specifies the unique identifier of the certificate being added.</span></span>

<span data-ttu-id="300e4-125">Możesz zwrócić informacje o odcisku palca dotyczące certyfikatów przy użyciu polecenia programu Windows PowerShell podobnej do następującego:</span><span class="sxs-lookup"><span data-stu-id="300e4-125">You can return thumbprint information for your certificates by using a Windows PowerShell command similar to this:</span></span>

`Get-ChildItem -Path Cert:\LocalMachine\Root`

<span data-ttu-id="300e4-126">Powyższe polecenie zwraca informacje dotyczące wszystkich certyfikatów komputerów lokalnych znajdujących się w głównym magazynie certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="300e4-126">The preceding command returns information for all the Local Computer certificates found in the Root certificate store.</span></span>

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

### <span data-ttu-id="300e4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="300e4-127">CommonParameters</span></span>
<span data-ttu-id="300e4-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="300e4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="300e4-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="300e4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="300e4-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="300e4-130">INPUTS</span></span>

###  
<span data-ttu-id="300e4-131">To polecenie cmdlet nie akceptuje danych wejściowych potoku.</span><span class="sxs-lookup"><span data-stu-id="300e4-131">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="300e4-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="300e4-132">OUTPUTS</span></span>

###  
<span data-ttu-id="300e4-133">To polecenie cmdlet tworzy nowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVpnClientRevokedCertificate** .</span><span class="sxs-lookup"><span data-stu-id="300e4-133">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRevokedCertificate** object.</span></span>

## <span data-ttu-id="300e4-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="300e4-134">NOTES</span></span>

## <span data-ttu-id="300e4-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="300e4-135">RELATED LINKS</span></span>

[<span data-ttu-id="300e4-136">Dodaj-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="300e4-136">Add-AzureRmVpnClientRevokedCertificate</span></span>](./Add-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="300e4-137">Get-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="300e4-137">Get-AzureRmVpnClientRevokedCertificate</span></span>](./Get-AzureRmVpnClientRevokedCertificate.md)

[<span data-ttu-id="300e4-138">Remove-AzureRmVpnClientRevokedCertificate</span><span class="sxs-lookup"><span data-stu-id="300e4-138">Remove-AzureRmVpnClientRevokedCertificate</span></span>](./Remove-AzureRmVpnClientRevokedCertificate.md)

