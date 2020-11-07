---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateorganizationdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetails.md
ms.openlocfilehash: 76208f8d4c1b8b1b463ea5a0f24a4e34e7a82855
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893038"
---
# <span data-ttu-id="6632a-101">New-AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="6632a-101">New-AzKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="6632a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6632a-102">SYNOPSIS</span></span>
<span data-ttu-id="6632a-103">Tworzy obiekt szczegółów organizacji certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="6632a-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="6632a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6632a-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6632a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6632a-105">DESCRIPTION</span></span>
<span data-ttu-id="6632a-106">Polecenie cmdlet **New-AzKeyVaultCertificateOrganizationDetails** umożliwia utworzenie obiektu szczegółów organizacji certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="6632a-106">The **New-AzKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="6632a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6632a-107">EXAMPLES</span></span>

### <span data-ttu-id="6632a-108">Przykład 1: Tworzenie obiektu szczegółów organizacji</span><span class="sxs-lookup"><span data-stu-id="6632a-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="6632a-109">Pierwsze polecenie powoduje utworzenie obiektu szczegółów administratora certyfikatu, a następnie zapisanie go w zmiennej $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="6632a-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="6632a-110">Drugie polecenie tworzy obiekt szczegóły organizacji certyfikatu, a następnie zapisuje go w zmiennej $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="6632a-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="6632a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6632a-111">PARAMETERS</span></span>

### <span data-ttu-id="6632a-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="6632a-112">-AdministratorDetails</span></span>
<span data-ttu-id="6632a-113">Określa administratorów organizacji certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="6632a-113">Specifies the certificate organization administrators.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6632a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6632a-114">-DefaultProfile</span></span>
<span data-ttu-id="6632a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6632a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6632a-116">-ID</span><span class="sxs-lookup"><span data-stu-id="6632a-116">-Id</span></span>
<span data-ttu-id="6632a-117">Określa identyfikator organizacji.</span><span class="sxs-lookup"><span data-stu-id="6632a-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="6632a-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6632a-118">-Confirm</span></span>
<span data-ttu-id="6632a-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6632a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6632a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6632a-120">-WhatIf</span></span>
<span data-ttu-id="6632a-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6632a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6632a-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6632a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6632a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6632a-123">CommonParameters</span></span>
<span data-ttu-id="6632a-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6632a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6632a-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6632a-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6632a-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6632a-126">INPUTS</span></span>

### <span data-ttu-id="6632a-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6632a-127">None</span></span>
<span data-ttu-id="6632a-128">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="6632a-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6632a-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6632a-129">OUTPUTS</span></span>

### <span data-ttu-id="6632a-130">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="6632a-130">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="6632a-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6632a-131">NOTES</span></span>

## <span data-ttu-id="6632a-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6632a-132">RELATED LINKS</span></span>

[<span data-ttu-id="6632a-133">Nowe — AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="6632a-133">New-AzKeyVaultCertificateAdministratorDetails</span></span>](./New-AzKeyVaultCertificateAdministratorDetails.md)

