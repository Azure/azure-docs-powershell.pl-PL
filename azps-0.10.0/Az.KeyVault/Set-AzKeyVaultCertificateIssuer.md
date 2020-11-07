---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 97faf51b25ee2ae36b028e4a6b992416949a219f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893017"
---
# <span data-ttu-id="2f277-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2f277-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2f277-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f277-102">SYNOPSIS</span></span>
<span data-ttu-id="2f277-103">Ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="2f277-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="2f277-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f277-104">SYNTAX</span></span>

### <span data-ttu-id="2f277-105">Rozwinięty (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2f277-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f277-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="2f277-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f277-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2f277-107">DESCRIPTION</span></span>
<span data-ttu-id="2f277-108">Polecenie cmdlet Set-AzKeyVaultCertificateIssuer ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="2f277-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="2f277-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f277-109">EXAMPLES</span></span>

### <span data-ttu-id="2f277-110">Przykład 1: Ustawianie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="2f277-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="2f277-111">To polecenie ustawia właściwości dla wystawcy certyfikatu, a następnie zapisuje je w zmiennej $Issuer.</span><span class="sxs-lookup"><span data-stu-id="2f277-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="2f277-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f277-112">PARAMETERS</span></span>

### <span data-ttu-id="2f277-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="2f277-113">-AccountId</span></span>
<span data-ttu-id="2f277-114">Określa identyfikator konta dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="2f277-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f277-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="2f277-115">-ApiKey</span></span>
<span data-ttu-id="2f277-116">Określa klucz interfejsu API dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="2f277-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f277-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f277-117">-DefaultProfile</span></span>
<span data-ttu-id="2f277-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2f277-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f277-119">— Wystawca</span><span class="sxs-lookup"><span data-stu-id="2f277-119">-Issuer</span></span>
<span data-ttu-id="2f277-120">Określa wystawcę certyfikatu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="2f277-120">Specifies the certificate issuer to update.</span></span>

```yaml
Type: KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f277-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="2f277-121">-IssuerProvider</span></span>
<span data-ttu-id="2f277-122">Określa typ wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="2f277-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f277-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2f277-123">-Name</span></span>
<span data-ttu-id="2f277-124">Określa nazwę emitenta.</span><span class="sxs-lookup"><span data-stu-id="2f277-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f277-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="2f277-125">-OrganizationDetails</span></span>
<span data-ttu-id="2f277-126">Szczegóły organizacji, które mają być używane z wystawcą.</span><span class="sxs-lookup"><span data-stu-id="2f277-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f277-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f277-127">-PassThru</span></span>
<span data-ttu-id="2f277-128">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2f277-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2f277-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2f277-129">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f277-130">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="2f277-130">-VaultName</span></span>
<span data-ttu-id="2f277-131">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="2f277-131">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f277-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f277-132">-Confirm</span></span>
<span data-ttu-id="2f277-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f277-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f277-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f277-134">-WhatIf</span></span>
<span data-ttu-id="2f277-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f277-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f277-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f277-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f277-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f277-137">CommonParameters</span></span>
<span data-ttu-id="2f277-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f277-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f277-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f277-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f277-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f277-140">INPUTS</span></span>

### <span data-ttu-id="2f277-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2f277-141">None</span></span>
<span data-ttu-id="2f277-142">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="2f277-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2f277-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f277-143">OUTPUTS</span></span>

### <span data-ttu-id="2f277-144">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="2f277-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="2f277-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f277-145">NOTES</span></span>

## <span data-ttu-id="2f277-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f277-146">RELATED LINKS</span></span>

[<span data-ttu-id="2f277-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2f277-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="2f277-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2f277-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

