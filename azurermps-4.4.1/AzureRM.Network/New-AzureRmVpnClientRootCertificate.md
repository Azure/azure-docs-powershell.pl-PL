---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVpnClientRootCertificate.md
ms.openlocfilehash: 941be726f2b7c7aaf3ebf3d4cef0a91239e88214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527401"
---
# <span data-ttu-id="f58b3-101">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f58b3-101">New-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="f58b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f58b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f58b3-103">Tworzy nowy certyfikat główny klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="f58b3-103">Creates a new VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f58b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f58b3-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f58b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f58b3-105">DESCRIPTION</span></span>
<span data-ttu-id="f58b3-106">Polecenie cmdlet **New-AzureRmVpnClientRootCertificate** tworzy nowy certyfikat główny sieci VPN do użytku w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f58b3-106">The **New-AzureRmVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="f58b3-107">Certyfikaty główne to certyfikaty X. 509, które identyfikują główny urząd certyfikacji: wszystkie inne certyfikaty używane w bramie ufają certyfikatowi głównemu.</span><span class="sxs-lookup"><span data-stu-id="f58b3-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="f58b3-108">To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f58b3-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="f58b3-109">Zamiast tego certyfikat utworzony za pomocą polecenia **New-AzureRmVpnClientRootCertificate** jest wykorzystywany w połączeniu z poleceniem cmdlet New-AzureRmVirtualNetworkGateway podczas tworzenia nowej bramy.</span><span class="sxs-lookup"><span data-stu-id="f58b3-109">Instead, the certificate created by **New-AzureRmVpnClientRootCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="f58b3-110">Załóżmy na przykład, że tworzysz nowy certyfikat i zapisujesz go w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="f58b3-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="f58b3-111">Po utworzeniu nowej bramy wirtualnej można użyć tego obiektu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f58b3-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="f58b3-112">Na przykład</span><span class="sxs-lookup"><span data-stu-id="f58b3-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

<span data-ttu-id="f58b3-113">Aby uzyskać więcej informacji, zobacz dokumentację New-AzureRmVirtualNetworkGateway polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f58b3-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="f58b3-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f58b3-114">EXAMPLES</span></span>

### <span data-ttu-id="f58b3-115">Przykład 1: Tworzenie certyfikatu głównego aclient</span><span class="sxs-lookup"><span data-stu-id="f58b3-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="f58b3-116">W tym przykładzie przedstawiono Tworzenie certyfikatu głównego klienta i przechowywanie obiektu Certificate w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="f58b3-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="f58b3-117">Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzureRmVirtualNetworkGateway** w celu dodania certyfikatu głównego do nowej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f58b3-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>

<span data-ttu-id="f58b3-118">W pierwszym poleceniu jest używane polecenie **Get-Content** , aby uzyskać uprzednio wyeksportowany tekst reprezentujący certyfikat główny. dane tekstowe są przechowywane w zmiennej o nazwie $Text.</span><span class="sxs-lookup"><span data-stu-id="f58b3-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>

<span data-ttu-id="f58b3-119">Drugie polecenie używa pętli for w celu wyodrębnienia całego tekstu z wyjątkiem pierwszego wiersza i ostatniego wiersza, przechowując wyodrębniony tekst w zmiennej o nazwie $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="f58b3-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>

<span data-ttu-id="f58b3-120">W trzecim poleceniu użyto polecenia cmdlet **New-AzureRmVpnClientRootCertificate** , aby utworzyć certyfikat, przechowując utworzony obiekt w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="f58b3-120">The third command uses the **New-AzureRmVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="f58b3-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f58b3-121">PARAMETERS</span></span>

### <span data-ttu-id="f58b3-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f58b3-122">-Name</span></span>
<span data-ttu-id="f58b3-123">Określa nazwę nowego certyfikatu głównego klienta.</span><span class="sxs-lookup"><span data-stu-id="f58b3-123">Specifies a name for the new client root certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f58b3-124">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="f58b3-124">-PublicCertData</span></span>
<span data-ttu-id="f58b3-125">Określa tekstową reprezentację głównego certyfikatu do dodania.</span><span class="sxs-lookup"><span data-stu-id="f58b3-125">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="f58b3-126">Aby otrzymać reprezentację tekstową, wyeksportuj certyfikat w formacie CER (przy użyciu kodowania base64), a następnie otwórz wynikowy plik w edytorze tekstów.</span><span class="sxs-lookup"><span data-stu-id="f58b3-126">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="f58b3-127">Powinno być wyświetlane dane wyjściowe podobne do tego (Zauważ, że rzeczywista produkcja zawiera więcej niż jeden wiersz tekstu niż w skróconym przykładzie przedstawionym poniżej):</span><span class="sxs-lookup"><span data-stu-id="f58b3-127">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="f58b3-128">-----ROZPOCZYNAć certyfikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----koniec certyfikatu-----</span><span class="sxs-lookup"><span data-stu-id="f58b3-128">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="f58b3-129">PublicCertData składa się ze wszystkich linii między pierwszym wierszem (-----ROZPOCZYNAć certyfikat-----) oraz ostatniego wiersza (-----końcowy certyfikat-----) w pliku.</span><span class="sxs-lookup"><span data-stu-id="f58b3-129">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="f58b3-130">Możesz pobrać PublicCertData, używając poleceń programu Windows PowerShell podobnych do tego:</span><span class="sxs-lookup"><span data-stu-id="f58b3-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="f58b3-131">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="f58b3-131">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="f58b3-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f58b3-132">-DefaultProfile</span></span>
<span data-ttu-id="f58b3-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f58b3-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f58b3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f58b3-134">CommonParameters</span></span>
<span data-ttu-id="f58b3-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f58b3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f58b3-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f58b3-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f58b3-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f58b3-137">INPUTS</span></span>

###  
<span data-ttu-id="f58b3-138">To polecenie cmdlet nie akceptuje danych wejściowych potoku.</span><span class="sxs-lookup"><span data-stu-id="f58b3-138">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="f58b3-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f58b3-139">OUTPUTS</span></span>

###  
<span data-ttu-id="f58b3-140">To polecenie cmdlet tworzy nowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVpnClientRootCertificate** .</span><span class="sxs-lookup"><span data-stu-id="f58b3-140">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="f58b3-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f58b3-141">NOTES</span></span>

## <span data-ttu-id="f58b3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f58b3-142">RELATED LINKS</span></span>

[<span data-ttu-id="f58b3-143">Dodaj-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f58b3-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="f58b3-144">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f58b3-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="f58b3-145">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="f58b3-145">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


