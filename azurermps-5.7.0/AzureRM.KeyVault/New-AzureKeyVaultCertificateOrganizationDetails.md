---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 3ece43bb0c1d4c97c5d1956a25707c920215781c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554145"
---
# <span data-ttu-id="84a6d-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="84a6d-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="84a6d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="84a6d-103">Tworzy obiekt szczegółów organizacji certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="84a6d-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84a6d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84a6d-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84a6d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84a6d-105">DESCRIPTION</span></span>
<span data-ttu-id="84a6d-106">Polecenie cmdlet **New-AzureKeyVaultCertificateOrganizationDetails** umożliwia utworzenie obiektu szczegółów organizacji certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="84a6d-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="84a6d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84a6d-107">EXAMPLES</span></span>

### <span data-ttu-id="84a6d-108">Przykład 1: Tworzenie obiektu szczegółów organizacji</span><span class="sxs-lookup"><span data-stu-id="84a6d-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="84a6d-109">Pierwsze polecenie powoduje utworzenie obiektu szczegółów administratora certyfikatu, a następnie zapisanie go w zmiennej $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="84a6d-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="84a6d-110">Drugie polecenie tworzy obiekt szczegóły organizacji certyfikatu, a następnie zapisuje go w zmiennej $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="84a6d-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="84a6d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84a6d-111">PARAMETERS</span></span>

### <span data-ttu-id="84a6d-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="84a6d-112">-AdministratorDetails</span></span>
<span data-ttu-id="84a6d-113">Określa administratorów organizacji certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="84a6d-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84a6d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84a6d-114">-DefaultProfile</span></span>
<span data-ttu-id="84a6d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="84a6d-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84a6d-116">-ID</span><span class="sxs-lookup"><span data-stu-id="84a6d-116">-Id</span></span>
<span data-ttu-id="84a6d-117">Określa identyfikator organizacji.</span><span class="sxs-lookup"><span data-stu-id="84a6d-117">Specifies the identifier for the organization.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84a6d-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="84a6d-118">-Confirm</span></span>
<span data-ttu-id="84a6d-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84a6d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84a6d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84a6d-120">-WhatIf</span></span>
<span data-ttu-id="84a6d-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84a6d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84a6d-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="84a6d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84a6d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84a6d-123">CommonParameters</span></span>
<span data-ttu-id="84a6d-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84a6d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84a6d-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84a6d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84a6d-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84a6d-126">INPUTS</span></span>

### <span data-ttu-id="84a6d-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="84a6d-127">None</span></span>
<span data-ttu-id="84a6d-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="84a6d-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="84a6d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84a6d-129">OUTPUTS</span></span>

### <span data-ttu-id="84a6d-130">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="84a6d-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="84a6d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84a6d-131">NOTES</span></span>

## <span data-ttu-id="84a6d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84a6d-132">RELATED LINKS</span></span>

[<span data-ttu-id="84a6d-133">Nowe — AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="84a6d-133">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)
