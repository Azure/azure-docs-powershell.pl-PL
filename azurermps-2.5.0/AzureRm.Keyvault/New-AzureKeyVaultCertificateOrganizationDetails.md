---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateorganizationdetails
schema: 2.0.0
ms.openlocfilehash: 76e0d37ac38c8b9799093ff3a4f4ea10c2fce2f4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898913"
---
# <span data-ttu-id="74ed3-101">New-AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="74ed3-101">New-AzureKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="74ed3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74ed3-102">SYNOPSIS</span></span>
<span data-ttu-id="74ed3-103">Tworzy obiekt szczegółów organizacji certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="74ed3-103">Creates an in-memory certificate organization details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74ed3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74ed3-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateOrganizationDetails [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74ed3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="74ed3-105">DESCRIPTION</span></span>
<span data-ttu-id="74ed3-106">Polecenie cmdlet **New-AzureKeyVaultCertificateOrganizationDetails** umożliwia utworzenie obiektu szczegółów organizacji certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="74ed3-106">The **New-AzureKeyVaultCertificateOrganizationDetails** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="74ed3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74ed3-107">EXAMPLES</span></span>

### <span data-ttu-id="74ed3-108">Przykład 1: Tworzenie obiektu szczegółów organizacji</span><span class="sxs-lookup"><span data-stu-id="74ed3-108">Example 1: Create an organization details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
$OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -Name "Contoso" -Address1 "1 Redmond Way" -Address2 "Suite 906" -City "Redmond" -State "WA" -Zip 98052 -Country "US" -AdministratorDetails $AdminDetails
```

<span data-ttu-id="74ed3-109">Pierwsze polecenie powoduje utworzenie obiektu szczegółów administratora certyfikatu, a następnie zapisanie go w zmiennej $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="74ed3-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

<span data-ttu-id="74ed3-110">Drugie polecenie tworzy obiekt szczegóły organizacji certyfikatu, a następnie zapisuje go w zmiennej $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="74ed3-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="74ed3-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74ed3-111">PARAMETERS</span></span>

### <span data-ttu-id="74ed3-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="74ed3-112">-AdministratorDetails</span></span>
<span data-ttu-id="74ed3-113">Określa administratorów organizacji certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="74ed3-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="74ed3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74ed3-114">-DefaultProfile</span></span>
<span data-ttu-id="74ed3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="74ed3-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74ed3-116">-ID</span><span class="sxs-lookup"><span data-stu-id="74ed3-116">-Id</span></span>
<span data-ttu-id="74ed3-117">Określa identyfikator organizacji.</span><span class="sxs-lookup"><span data-stu-id="74ed3-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="74ed3-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74ed3-118">-Confirm</span></span>
<span data-ttu-id="74ed3-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ed3-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74ed3-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74ed3-120">-WhatIf</span></span>
<span data-ttu-id="74ed3-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74ed3-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74ed3-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="74ed3-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74ed3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74ed3-123">CommonParameters</span></span>
<span data-ttu-id="74ed3-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74ed3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74ed3-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74ed3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74ed3-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74ed3-126">INPUTS</span></span>

## <span data-ttu-id="74ed3-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74ed3-127">OUTPUTS</span></span>

### <span data-ttu-id="74ed3-128">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="74ed3-128">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="74ed3-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74ed3-129">NOTES</span></span>

## <span data-ttu-id="74ed3-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74ed3-130">RELATED LINKS</span></span>

[<span data-ttu-id="74ed3-131">Nowe — AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="74ed3-131">New-AzureKeyVaultCertificateAdministratorDetails</span></span>](./New-AzureKeyVaultCertificateAdministratorDetails.md)

