---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: eac75ae5c9828493244ace01b6c090fda7e6ef5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549168"
---
# <span data-ttu-id="02c75-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="02c75-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="02c75-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02c75-102">SYNOPSIS</span></span>
<span data-ttu-id="02c75-103">Ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="02c75-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02c75-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02c75-104">SYNTAX</span></span>

### <span data-ttu-id="02c75-105">Rozwinięty (domyślny)</span><span class="sxs-lookup"><span data-stu-id="02c75-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c75-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="02c75-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c75-107">Opis</span><span class="sxs-lookup"><span data-stu-id="02c75-107">DESCRIPTION</span></span>
<span data-ttu-id="02c75-108">Polecenie cmdlet Set-AzureKeyVaultCertificateIssuer ustawia wystawcę certyfikatu w magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="02c75-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="02c75-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02c75-109">EXAMPLES</span></span>

### <span data-ttu-id="02c75-110">Przykład 1: Ustawianie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="02c75-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="02c75-111">To polecenie ustawia właściwości dla wystawcy certyfikatu, a następnie zapisuje je w zmiennej $Issuer.</span><span class="sxs-lookup"><span data-stu-id="02c75-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="02c75-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02c75-112">PARAMETERS</span></span>

### <span data-ttu-id="02c75-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="02c75-113">-AccountId</span></span>
<span data-ttu-id="02c75-114">Określa identyfikator konta dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="02c75-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c75-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="02c75-115">-ApiKey</span></span>
<span data-ttu-id="02c75-116">Określa klucz interfejsu API dla wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="02c75-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c75-117">— Wystawca</span><span class="sxs-lookup"><span data-stu-id="02c75-117">-Issuer</span></span>
<span data-ttu-id="02c75-118">Określa wystawcę certyfikatu do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="02c75-118">Specifies the certificate issuer to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c75-119">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="02c75-119">-IssuerProvider</span></span>
<span data-ttu-id="02c75-120">Określa typ wystawcy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="02c75-120">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c75-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="02c75-121">-Name</span></span>
<span data-ttu-id="02c75-122">Określa nazwę emitenta.</span><span class="sxs-lookup"><span data-stu-id="02c75-122">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c75-123">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="02c75-123">-OrganizationDetails</span></span>
<span data-ttu-id="02c75-124">Szczegóły organizacji, które mają być używane z wystawcą.</span><span class="sxs-lookup"><span data-stu-id="02c75-124">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c75-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02c75-125">-PassThru</span></span>
<span data-ttu-id="02c75-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="02c75-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02c75-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="02c75-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c75-128">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="02c75-128">-VaultName</span></span>
<span data-ttu-id="02c75-129">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="02c75-129">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02c75-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02c75-130">-Confirm</span></span>
<span data-ttu-id="02c75-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02c75-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c75-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c75-132">-WhatIf</span></span>
<span data-ttu-id="02c75-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02c75-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02c75-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02c75-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02c75-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c75-135">-DefaultProfile</span></span>
<span data-ttu-id="02c75-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02c75-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02c75-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c75-137">CommonParameters</span></span>
<span data-ttu-id="02c75-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02c75-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c75-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c75-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c75-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02c75-140">INPUTS</span></span>

## <span data-ttu-id="02c75-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02c75-141">OUTPUTS</span></span>

### <span data-ttu-id="02c75-142">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="02c75-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="02c75-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02c75-143">NOTES</span></span>

## <span data-ttu-id="02c75-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02c75-144">RELATED LINKS</span></span>

[<span data-ttu-id="02c75-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="02c75-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="02c75-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="02c75-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

