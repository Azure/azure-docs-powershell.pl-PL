---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5D857FF6-A27D-4031-948D-8A69D24B4AD4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnclientrootcertificate
schema: 2.0.0
ms.openlocfilehash: 66c026e3e1ec05d94b8dc19b2ceedd92d4fc0200
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899085"
---
# <span data-ttu-id="506f8-101">Remove-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="506f8-101">Remove-AzureRmVpnClientRootCertificate</span></span>

## <span data-ttu-id="506f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="506f8-102">SYNOPSIS</span></span>
<span data-ttu-id="506f8-103">Usuwa istniejący certyfikat główny klienta VPN.</span><span class="sxs-lookup"><span data-stu-id="506f8-103">Removes an existing VPN client root certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="506f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="506f8-104">SYNTAX</span></span>

```
Remove-AzureRmVpnClientRootCertificate -VpnClientRootCertificateName <String>
 -VirtualNetworkGatewayName <String> -ResourceGroupName <String> -PublicCertData <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="506f8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="506f8-105">DESCRIPTION</span></span>
<span data-ttu-id="506f8-106">Polecenie cmdlet **Remove-AzureRmVpnClientRootCertificate** usuwa określony certyfikat główny z bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="506f8-106">The **Remove-AzureRmVpnClientRootCertificate** cmdlet removes the specified root certificate from a virtual network gateway.</span></span>
<span data-ttu-id="506f8-107">Certyfikaty główne to certyfikaty X. 509, które identyfikują główny urząd certyfikacji: wszystkie inne certyfikaty używane w bramie ufają certyfikatowi głównemu.</span><span class="sxs-lookup"><span data-stu-id="506f8-107">Root certificates are X.509 certificates that identify your Root Certification Authority: all other certificates used on the gateway trust the root certificate.</span></span>
<span data-ttu-id="506f8-108">Po usunięciu komputerów z certyfikatem głównym korzystającym z certyfikatu do celów uwierzytelnienia nie będzie już można połączyć się z bramą.</span><span class="sxs-lookup"><span data-stu-id="506f8-108">If you remove a root certificate computers that use the certificate for authentication purposes will no longer be able to connect to the gateway.</span></span>

<span data-ttu-id="506f8-109">W przypadku korzystania z funkcji **Remove-AzureRmVpnClientRootCertificate** należy podać zarówno nazwę certyfikatu, jak i tekstową reprezentację danych certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="506f8-109">When you use **Remove-AzureRmVpnClientRootCertificate** , you must supply both the certificate name and a text representation of the certificate data.</span></span>
<span data-ttu-id="506f8-110">Aby uzyskać więcej informacji na temat reprezentacji tekstu certyfikatu, zobacz opis parametru *PublicCertData* .</span><span class="sxs-lookup"><span data-stu-id="506f8-110">For more information about the text representation of a certificate see the *PublicCertData* parameter description.</span></span>

## <span data-ttu-id="506f8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="506f8-111">EXAMPLES</span></span>

### <span data-ttu-id="506f8-112">Przykład 1: Usuwanie certyfikatu głównego klienta z bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="506f8-112">Example 1: Remove a client root certificate from a virtual network gateway</span></span>
```
PS C:\>$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer"
PS C:\> $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text[$i]}
PS C:\> Remove-AzureRmVpnClientRootCertificate -PublicCertData $CertificateText -ResourceGroupName "ContosoResourceGroup" -VirtualNetworkGatewayName "ContosoVirtualGateway"-VpnClientRootCertificateName "ContosoRootCertificate"
```

<span data-ttu-id="506f8-113">W tym przykładzie usunięto certyfikat główny klienta o nazwie ContosoRootCertificate z ContosoVirtualGateway bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="506f8-113">This example removes a client root certificate named ContosoRootCertificate from the virtual network gateway ContosoVirtualGateway.</span></span>

<span data-ttu-id="506f8-114">W pierwszym poleceniu jest używane polecenie **Get-Content** , które pozwala uzyskać uprzednio wyeksportowany tekst przedstawiający reprezentację certyfikatu. Ta Reprezentacja tekstowa jest przechowywana w zmiennej o nazwie $Text.</span><span class="sxs-lookup"><span data-stu-id="506f8-114">The first command uses the **Get-Content** cmdlet to get a previously-exported text representation of the certificate; this text representation is stored in a variable named $Text.</span></span>

<span data-ttu-id="506f8-115">Drugie polecenie używa pętli for w celu wyodrębnienia całego tekstu w $Text z wyjątkiem pierwszego wiersza i ostatniego wiersza.</span><span class="sxs-lookup"><span data-stu-id="506f8-115">The second command then uses a for loop to extract all the text in $Text except for the first line and the last line.</span></span>
<span data-ttu-id="506f8-116">Ten wyodrębniony tekst jest przechowywany w zmiennej o nazwie $CertificateText.</span><span class="sxs-lookup"><span data-stu-id="506f8-116">This extracted text is stored in a variable named $CertificateText.</span></span>

<span data-ttu-id="506f8-117">W trzecim poleceniu są używane informacje przechowywane w zmiennej $CertificateText wraz z poleceniem cmdlet **Remove-AzureRmVpnClientRootCertificate** w celu usunięcia certyfikatu z bramy.</span><span class="sxs-lookup"><span data-stu-id="506f8-117">The third command uses the information stored in the $CertificateText variable along with the **Remove-AzureRmVpnClientRootCertificate** cmdlet to remove the certificate from the gateway.</span></span>

## <span data-ttu-id="506f8-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="506f8-118">PARAMETERS</span></span>

### <span data-ttu-id="506f8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506f8-119">-DefaultProfile</span></span>
<span data-ttu-id="506f8-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="506f8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="506f8-121">-PublicCertData</span><span class="sxs-lookup"><span data-stu-id="506f8-121">-PublicCertData</span></span>
<span data-ttu-id="506f8-122">Określa tekstową reprezentację głównego certyfikatu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="506f8-122">Specifies the text representation of the root certificate to be removed.</span></span>
<span data-ttu-id="506f8-123">Aby otrzymać reprezentację tekstową, wyeksportuj certyfikat w formacie CER (przy użyciu kodowania base64), a następnie otwórz wynikowy plik w edytorze tekstów.</span><span class="sxs-lookup"><span data-stu-id="506f8-123">To obtain the text representation, export your certificate in .cer format (using Base64) encoding, then open the resulting file in a text editor.</span></span>
<span data-ttu-id="506f8-124">Powinno być wyświetlane dane wyjściowe podobne do poniższych (Zauważ, że rzeczywista produkcja zawiera więcej niż jeden wiersz tekstu niż skrót przedstawiony tutaj):</span><span class="sxs-lookup"><span data-stu-id="506f8-124">You should see output similar to the following (note that the actual output will contain many more lines of text than the abbreviated sample shown here):</span></span>

<span data-ttu-id="506f8-125">-----ROZPOCZYNAć certyfikat-----MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w-----koniec certyfikatu-----</span><span class="sxs-lookup"><span data-stu-id="506f8-125">----- BEGIN CERTIFICATE ----- MIIC13FAAXC3671Auij9HHgUNEW8343NMJklo09982CVVFAw8w ----- END CERTIFICATE -----</span></span>

<span data-ttu-id="506f8-126">PublicCertData składa się ze wszystkich linii między pierwszym wierszem (-----ROZPOCZYNAć certyfikat-----) oraz ostatniego wiersza (-----końcowy certyfikat-----) w pliku.</span><span class="sxs-lookup"><span data-stu-id="506f8-126">The PublicCertData is made up of all the lines between the first line (----- BEGIN CERTIFICATE -----) and the last line (----- END CERTIFICATE -----) in the file.</span></span>
<span data-ttu-id="506f8-127">PublicCertData można pobrać za pomocą poleceń programu Windows PowerShell podobnych do tego:</span><span class="sxs-lookup"><span data-stu-id="506f8-127">You can retrieve the PublicCertData using Windows PowerShell commands similar to this:</span></span>

<span data-ttu-id="506f8-128">$Text = Get-Content-Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i = 1; $i-lt $Text. length-1; $i + +) {$Text \[ $i \] }</span><span class="sxs-lookup"><span data-stu-id="506f8-128">$Text = Get-Content -Path "C:\Azure\Certificates\ExportedCertficate.cer" $CertificateText = for ($i=1; $i -lt $Text.Length -1 ; $i++){$Text\[$i\]}</span></span>

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

### <span data-ttu-id="506f8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="506f8-129">-ResourceGroupName</span></span>
<span data-ttu-id="506f8-130">Określa nazwę grupy zasobów, do której jest przypisana Brama sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="506f8-130">Specifies the name of the resource group that the virtual network gateway is assigned to.</span></span>

<span data-ttu-id="506f8-131">Grupy zasobów umożliwiają Kategoryzowanie elementów w celu uproszczenia zarządzania zapasami i ogólnego administrowania usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="506f8-131">Resource groups categorize items to help simplify inventory management and general Azure administration.</span></span>

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

### <span data-ttu-id="506f8-132">-VirtualNetworkGatewayName</span><span class="sxs-lookup"><span data-stu-id="506f8-132">-VirtualNetworkGatewayName</span></span>
<span data-ttu-id="506f8-133">Określa nazwę bramy sieci wirtualnej, z której jest usuwany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="506f8-133">Specifies the name of the virtual network gateway that the certificate is removed from.</span></span>

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

### <span data-ttu-id="506f8-134">-VpnClientRootCertificateName</span><span class="sxs-lookup"><span data-stu-id="506f8-134">-VpnClientRootCertificateName</span></span>
<span data-ttu-id="506f8-135">Określa nazwę certyfikatu głównego klienta, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="506f8-135">Specifies the name of the client root certificate that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="506f8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506f8-136">CommonParameters</span></span>
<span data-ttu-id="506f8-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="506f8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506f8-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="506f8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506f8-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="506f8-139">INPUTS</span></span>

## <span data-ttu-id="506f8-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="506f8-140">OUTPUTS</span></span>

## <span data-ttu-id="506f8-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="506f8-141">NOTES</span></span>

## <span data-ttu-id="506f8-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="506f8-142">RELATED LINKS</span></span>

[<span data-ttu-id="506f8-143">Dodaj-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="506f8-143">Add-AzureRmVpnClientRootCertificate</span></span>](./Add-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="506f8-144">Get-AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="506f8-144">Get-AzureRmVpnClientRootCertificate</span></span>](./Get-AzureRmVpnClientRootCertificate.md)

[<span data-ttu-id="506f8-145">Nowe — AzureRmVpnClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="506f8-145">New-AzureRmVpnClientRootCertificate</span></span>](./New-AzureRmVpnClientRootCertificate.md)


