---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: a5f562fd05432abc502d648ca7fae614744e4f2c
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899101"
---
# <span data-ttu-id="6aa69-101">New-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6aa69-101">New-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="6aa69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6aa69-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa69-103">Tworzy nowy certyfikat główny klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="6aa69-103">Creates a new VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6aa69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6aa69-104">SYNTAX</span></span>

```
New-AzureRmVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aa69-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6aa69-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa69-106">Polecenie cmdlet **New-AzureRmVpnClientRootCertificate** tworzy nowy certyfikat główny sieci VPN do użytku w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6aa69-106">The **New-AzureRmVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="6aa69-107">Certyfikaty główne to certyfikaty X. 509, które identyfikują główny urząd certyfikacji: wszystkie inne certyfikaty używane w bramie ufają certyfikatowi głównemu.</span><span class="sxs-lookup"><span data-stu-id="6aa69-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>

<span data-ttu-id="6aa69-108">To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6aa69-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="6aa69-109">Zamiast tego certyfikat utworzony za pomocą polecenia **New-AzureRmVpnClientRootCertificate** jest wykorzystywany w połączeniu z poleceniem cmdlet New-AzureRmVirtualNetworkGateway podczas tworzenia nowej bramy.</span><span class="sxs-lookup"><span data-stu-id="6aa69-109">Instead, the certificate created by **New-AzureRmVpnClientRootCertificate** is used in conjunction with the New-AzureRmVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="6aa69-110">Załóżmy na przykład, że tworzysz nowy certyfikat i zapisujesz go w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="6aa69-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="6aa69-111">Po utworzeniu nowej bramy wirtualnej można użyć tego obiektu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="6aa69-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="6aa69-112">Na przykład</span><span class="sxs-lookup"><span data-stu-id="6aa69-112">For instance,</span></span>

`New-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`

<span data-ttu-id="6aa69-113">Aby uzyskać więcej informacji, zobacz dokumentację New-AzureRmVirtualNetworkGateway polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aa69-113">For more information, see the documentation for the New-AzureRmVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="6aa69-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6aa69-114">EXAMPLES</span></span>

### <span data-ttu-id="6aa69-115">Przykład 1: Tworzenie certyfikatu głównego aclient</span><span class="sxs-lookup"><span data-stu-id="6aa69-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="6aa69-116">W tym przykładzie przedstawiono Tworzenie certyfikatu głównego klienta i przechowywanie obiektu Certificate w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="6aa69-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="6aa69-117">Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzureRmVirtualNetworkGateway** w celu dodania certyfikatu głównego do nowej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="6aa69-117">This variable can then be used by the **New-AzureRmVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>

<span data-ttu-id="6aa69-118">W pierwszym poleceniu jest używane polecenie **Get-Content** , aby uzyskać uprzednio wyeksportowany tekst reprezentujący certyfikat główny. dane tekstowe są przechowywane w zmiennej o nazwie $Text.</span><span class="sxs-lookup"><span data-stu-id="6aa69-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>

<span data-ttu-id="6aa69-119">Drugie polecenie używa pętli for w celu wyodrębnienia całego tekstu z wyjątkiem pierwszego wiersza i ostatniego wiersza, przechowując wyodrębniony tekst w zmiennej o nazwie $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="6aa69-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>

<span data-ttu-id="6aa69-120">W trzecim poleceniu użyto polecenia cmdlet **New-AzureRmVpnClientRootCertificate** , aby utworzyć certyfikat, przechowując utworzony obiekt w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="6aa69-120">The third command uses the **New-AzureRmVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="6aa69-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6aa69-121">PARAMETERS</span></span>

### <span data-ttu-id="6aa69-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa69-122">-DefaultProfile</span></span>
<span data-ttu-id="6aa69-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6aa69-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aa69-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6aa69-124">-Name</span></span>
<span data-ttu-id="6aa69-125">Określa nazwę nowego certyfikatu głównego klienta.</span><span class="sxs-lookup"><span data-stu-id="6aa69-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="6aa69-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="6aa69-126">-PublicCertData</span></span>
<span data-ttu-id="6aa69-127">Określa tekstową reprezentację głównego certyfikatu do dodania.</span><span class="sxs-lookup"><span data-stu-id="6aa69-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="6aa69-128">Aby otrzymać reprezentację tekstową, wyeksportuj certyfikat w formacie CER (przy użyciu kodowania base64), a następnie otwórz wynikowy plik w edytorze tekstów.</span><span class="sxs-lookup"><span data-stu-id="6aa69-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="6aa69-129">Powinno być wyświetlane dane wyjściowe podobne do tego (Zauważ, że rzeczywista produkcja zawiera więcej niż jeden wiersz tekstu niż w skróconym przykładzie przedstawionym poniżej):</span><span class="sxs-lookup"><span data-stu-id="6aa69-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="6aa69-130">-----ROZPOCZYNAć certyfikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----koniec certyfikatu-----</span><span class="sxs-lookup"><span data-stu-id="6aa69-130">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="6aa69-131">PublicCertData składa się ze wszystkich linii między pierwszym wierszem (-----ROZPOCZYNAć certyfikat-----) oraz ostatniego wiersza (-----końcowy certyfikat-----) w pliku.</span><span class="sxs-lookup"><span data-stu-id="6aa69-131">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="6aa69-132">Możesz pobrać PublicCertData, używając poleceń programu Windows PowerShell podobnych do tego:</span><span class="sxs-lookup"><span data-stu-id="6aa69-132">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="6aa69-133">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="6aa69-133">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aa69-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa69-134">CommonParameters</span></span>
<span data-ttu-id="6aa69-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aa69-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa69-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa69-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa69-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6aa69-137">INPUTS</span></span>

###  
<span data-ttu-id="6aa69-138">To polecenie cmdlet nie akceptuje danych wejściowych potoku.</span><span class="sxs-lookup"><span data-stu-id="6aa69-138">This cmdlet does not accept pipelined input.</span></span>

## <span data-ttu-id="6aa69-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6aa69-139">OUTPUTS</span></span>

###  
<span data-ttu-id="6aa69-140">To polecenie cmdlet tworzy nowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVpnClientRootCertificate** .</span><span class="sxs-lookup"><span data-stu-id="6aa69-140">This cmdlet creates new instances of the **Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate** object.</span></span>

## <span data-ttu-id="6aa69-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6aa69-141">NOTES</span></span>

## <span data-ttu-id="6aa69-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6aa69-142">RELATED LINKS</span></span>

[<span data-ttu-id="6aa69-143">Dodaj-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6aa69-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="6aa69-144">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6aa69-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="6aa69-145">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6aa69-145">Remove-AzureRmVpnClientRootCertificate</span></span>](./Remove-AzureRmVpnClientRootCertificate.md)


