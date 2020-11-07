---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C54AC64C-DA21-443E-8CFE-6CCAC6152C2B
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnclientrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnClientRootCertificate.md
ms.openlocfilehash: 4d05680951585f0b5271c291cb893a28f822a6fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709207"
---
# <span data-ttu-id="2165a-101">New-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2165a-101">New-AzVpnClientRootCertificate</span></span>

## <span data-ttu-id="2165a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2165a-102">SYNOPSIS</span></span>
<span data-ttu-id="2165a-103">Tworzy nowy certyfikat główny klienta sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="2165a-103">Creates a new VPN client root certificate.</span></span>

## <span data-ttu-id="2165a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2165a-104">SYNTAX</span></span>

```
New-AzVpnClientRootCertificate -Name <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2165a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2165a-105">DESCRIPTION</span></span>
<span data-ttu-id="2165a-106">Polecenie cmdlet **New-AzVpnClientRootCertificate** tworzy nowy certyfikat główny sieci VPN do użytku w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2165a-106">The **New-AzVpnClientRootCertificate** cmdlet creates a new VPN root certificate for use on a virtual network gateway.</span></span>
<span data-ttu-id="2165a-107">Certyfikaty główne to certyfikaty X. 509, które identyfikują główny urząd certyfikacji: wszystkie inne certyfikaty używane w bramie ufają certyfikatowi głównemu.</span><span class="sxs-lookup"><span data-stu-id="2165a-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="2165a-108">To polecenie cmdlet tworzy autonomiczny certyfikat, który nie jest przypisany do bramy wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2165a-108">This cmdlet creates a stand-alone certificate that is not assigned to a virtual gateway.</span></span>
<span data-ttu-id="2165a-109">Zamiast tego certyfikat utworzony za pomocą polecenia **New-AzVpnClientRootCertificate** jest wykorzystywany w połączeniu z poleceniem cmdlet New-AzVirtualNetworkGateway podczas tworzenia nowej bramy.</span><span class="sxs-lookup"><span data-stu-id="2165a-109">Instead, the certificate created by **New-AzVpnClientRootCertificate** is used in conjunction with the New-AzVirtualNetworkGateway cmdlet when creating a new gateway.</span></span>
<span data-ttu-id="2165a-110">Załóżmy na przykład, że tworzysz nowy certyfikat i zapisujesz go w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="2165a-110">For example, suppose you create a new certificate and store it in a variable named $Certificate.</span></span>
<span data-ttu-id="2165a-111">Po utworzeniu nowej bramy wirtualnej można użyć tego obiektu certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="2165a-111">You can then use that certificate object when creating a new virtual gateway.</span></span>
<span data-ttu-id="2165a-112">Na przykład `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span><span class="sxs-lookup"><span data-stu-id="2165a-112">For instance, `New-AzVirtualNetworkGateway -Name "ContosoVirtualGateway" -ResourceGroupName "ContosoResourceGroup" -Location "West US" -GatewayType "VPN" -IpConfigurations $Ipconfig  -VPNType "RouteBased" -VpnClientRootCertificates $Certificate`</span></span>
<span data-ttu-id="2165a-113">Aby uzyskać więcej informacji, zobacz dokumentację New-AzVirtualNetworkGateway polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2165a-113">For more information, see the documentation for the New-AzVirtualNetworkGateway cmdlet.</span></span>

## <span data-ttu-id="2165a-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2165a-114">EXAMPLES</span></span>

### <span data-ttu-id="2165a-115">Przykład 1: Tworzenie certyfikatu głównego aclient</span><span class="sxs-lookup"><span data-stu-id="2165a-115">Example 1: Create aclient root certificate</span></span>
```
PS C:\> $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> $Certificate = New-AzVpnClientRootCertificate -PublicCertData $CertificateText -Name "ContosoClientRootCertificate"
```

<span data-ttu-id="2165a-116">W tym przykładzie przedstawiono Tworzenie certyfikatu głównego klienta i przechowywanie obiektu Certificate w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="2165a-116">This example creates a client root certificate and store the certificate object in a variable named $Certificate.</span></span>
<span data-ttu-id="2165a-117">Ta zmienna może być następnie używana przez polecenie cmdlet **New-AzVirtualNetworkGateway** w celu dodania certyfikatu głównego do nowej bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2165a-117">This variable can then be used by the **New-AzVirtualNetworkGateway** cmdlet to add a root certificate to a new virtual network gateway.</span></span>
<span data-ttu-id="2165a-118">W pierwszym poleceniu jest używane polecenie **Get-Content** , aby uzyskać uprzednio wyeksportowany tekst reprezentujący certyfikat główny. dane tekstowe są przechowywane w zmiennej o nazwie $Text.</span><span class="sxs-lookup"><span data-stu-id="2165a-118">The first command uses the **Get-Content** cmdlet to get a previously exported text representation of the root certificate; that text data is stored in a variable named $Text.</span></span>
<span data-ttu-id="2165a-119">Drugie polecenie używa pętli for w celu wyodrębnienia całego tekstu z wyjątkiem pierwszego wiersza i ostatniego wiersza, przechowując wyodrębniony tekst w zmiennej o nazwie $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="2165a-119">The second command then uses a for loop to extract all the text except for the first line and the last line, storing the extracted text in a variable named $CertificateText.</span></span>
<span data-ttu-id="2165a-120">W trzecim poleceniu użyto polecenia cmdlet **New-AzVpnClientRootCertificate** , aby utworzyć certyfikat, przechowując utworzony obiekt w zmiennej o nazwie $Certificate.</span><span class="sxs-lookup"><span data-stu-id="2165a-120">The third command uses the **New-AzVpnClientRootCertificate** cmdlet to create the certificate, storing the created object in a variable named $Certificate.</span></span>

## <span data-ttu-id="2165a-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2165a-121">PARAMETERS</span></span>

### <span data-ttu-id="2165a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2165a-122">-DefaultProfile</span></span>
<span data-ttu-id="2165a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2165a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2165a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2165a-124">-Name</span></span>
<span data-ttu-id="2165a-125">Określa nazwę nowego certyfikatu głównego klienta.</span><span class="sxs-lookup"><span data-stu-id="2165a-125">Specifies a name for the new client root certificate.</span></span>

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

### <span data-ttu-id="2165a-126">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="2165a-126">-PublicCertData</span></span>
<span data-ttu-id="2165a-127">Określa tekstową reprezentację głównego certyfikatu do dodania.</span><span class="sxs-lookup"><span data-stu-id="2165a-127">Specifies a text representation of the root certificate to be added.</span></span>
<span data-ttu-id="2165a-128">Aby otrzymać reprezentację tekstową, wyeksportuj certyfikat w formacie CER (przy użyciu kodowania base64), a następnie otwórz wynikowy plik w edytorze tekstów.</span><span class="sxs-lookup"><span data-stu-id="2165a-128">To obtain the text representation, export your certificate in .cer format (using Base64 encoding), then open the resulting file in a text editor.</span></span>
<span data-ttu-id="2165a-129">Powinno być wyświetlane dane wyjściowe podobne do tego (Zauważ, że rzeczywista produkcja zawiera więcej niż jeden wiersz tekstu niż skrót skrócony):-----ROZPOCZYNAć certyfikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----Kończenie certyfikatu-----PublicCertData składa się ze wszystkich wierszy między pierwszym wierszem (-----Rozpocznij certyfikat-----) i ostatnim wierszem (----------końcowego certyfikatu) w pliku.</span><span class="sxs-lookup"><span data-stu-id="2165a-129">You should see output similar to this (note that the actual output will contain many more lines of text than the abbreviated sample shown here): ----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE ----- The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="2165a-130">Możesz pobrać PublicCertData, używając poleceń środowiska Windows PowerShell podobnych do tego: $Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="2165a-130">You can retrieve the PublicCertData by using Windows PowerShell commands similar to this: $Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="2165a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2165a-131">CommonParameters</span></span>
<span data-ttu-id="2165a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2165a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2165a-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2165a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2165a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2165a-134">INPUTS</span></span>

### <span data-ttu-id="2165a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2165a-135">System.String</span></span>

## <span data-ttu-id="2165a-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2165a-136">OUTPUTS</span></span>

### <span data-ttu-id="2165a-137">Microsoft. Azure. Commands. Network. models. PSVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2165a-137">Microsoft.Azure.Commands.Network.Models.PSVpnClientRootCertificate</span></span>

## <span data-ttu-id="2165a-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2165a-138">NOTES</span></span>

## <span data-ttu-id="2165a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2165a-139">RELATED LINKS</span></span>

[<span data-ttu-id="2165a-140">Dodaj-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2165a-140">Add-AzVpnClientRootCertificate</span></span>](./Add-AzVpnClientRootCertificate.md)

[<span data-ttu-id="2165a-141">Get-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2165a-141">Get-AzVpnClientRootCertificate</span></span>](./Get-AzVpnClientRootCertificate.md)

[<span data-ttu-id="2165a-142">Remove-AzVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="2165a-142">Remove-AzVpnClientRootCertificate</span></span>](./Remove-AzVpnClientRootCertificate.md)


