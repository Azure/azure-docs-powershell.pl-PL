---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 430a909e76c08ba0c19c18072fdf019cd2fa7b29
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898742"
---
# <span data-ttu-id="d7b41-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d7b41-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="d7b41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7b41-102">SYNOPSIS</span></span>
<span data-ttu-id="d7b41-103">Ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d7b41-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7b41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7b41-104">SYNTAX</span></span>

### <span data-ttu-id="d7b41-105">Rozwinięty (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d7b41-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7b41-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="d7b41-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7b41-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d7b41-107">DESCRIPTION</span></span>
<span data-ttu-id="d7b41-108">Polecenie cmdlet Set-AzureKeyVaultCertificateIssuer ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="d7b41-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="d7b41-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7b41-109">EXAMPLES</span></span>

### <span data-ttu-id="d7b41-110">Przykład 1: Ustawianie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="d7b41-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="d7b41-111">To polecenie ustawia właściwości dla wystawcy certyfikatu, a następnie zapisuje je w zmiennej $Issuer.</span><span class="sxs-lookup"><span data-stu-id="d7b41-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="d7b41-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7b41-112">PARAMETERS</span></span>

### <span data-ttu-id="d7b41-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="d7b41-113">-AccountId</span></span>
<span data-ttu-id="d7b41-114">Określa identyfikator konta dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d7b41-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="d7b41-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="d7b41-115">-ApiKey</span></span>
<span data-ttu-id="d7b41-116">Określa klucz interfejsu API dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d7b41-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="d7b41-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7b41-117">-DefaultProfile</span></span>
<span data-ttu-id="d7b41-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d7b41-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7b41-119">— Wystawca</span><span class="sxs-lookup"><span data-stu-id="d7b41-119">-Issuer</span></span>
<span data-ttu-id="d7b41-120">Określa wystawcę certyfikatu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="d7b41-120">Specifies the certificate issuer to update.</span></span>

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

### <span data-ttu-id="d7b41-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="d7b41-121">-IssuerProvider</span></span>
<span data-ttu-id="d7b41-122">Określa typ wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="d7b41-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="d7b41-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7b41-123">-Name</span></span>
<span data-ttu-id="d7b41-124">Określa nazwę emitenta.</span><span class="sxs-lookup"><span data-stu-id="d7b41-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="d7b41-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="d7b41-125">-OrganizationDetails</span></span>
<span data-ttu-id="d7b41-126">Szczegóły organizacji, które mają być używane z wystawcą.</span><span class="sxs-lookup"><span data-stu-id="d7b41-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="d7b41-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7b41-127">-PassThru</span></span>
<span data-ttu-id="d7b41-128">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d7b41-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d7b41-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d7b41-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d7b41-130">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="d7b41-130">-VaultName</span></span>
<span data-ttu-id="d7b41-131">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="d7b41-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="d7b41-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7b41-132">-Confirm</span></span>
<span data-ttu-id="d7b41-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7b41-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7b41-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7b41-134">-WhatIf</span></span>
<span data-ttu-id="d7b41-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7b41-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7b41-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7b41-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7b41-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7b41-137">CommonParameters</span></span>
<span data-ttu-id="d7b41-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7b41-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7b41-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7b41-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7b41-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7b41-140">INPUTS</span></span>

## <span data-ttu-id="d7b41-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7b41-141">OUTPUTS</span></span>

### <span data-ttu-id="d7b41-142">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="d7b41-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="d7b41-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7b41-143">NOTES</span></span>

## <span data-ttu-id="d7b41-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7b41-144">RELATED LINKS</span></span>

[<span data-ttu-id="d7b41-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d7b41-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="d7b41-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="d7b41-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

