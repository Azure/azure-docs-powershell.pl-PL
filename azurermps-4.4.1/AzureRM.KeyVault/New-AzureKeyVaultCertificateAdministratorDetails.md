---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/New-AzureKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 28a2bb0c806fa152a742c2fc9e36b150116a6352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527538"
---
# <span data-ttu-id="841b1-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="841b1-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="841b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="841b1-102">SYNOPSIS</span></span>
<span data-ttu-id="841b1-103">Tworzy obiekt szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="841b1-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="841b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="841b1-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="841b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="841b1-105">DESCRIPTION</span></span>
<span data-ttu-id="841b1-106">Polecenie cmdlet **New-AzureKeyVaultCertificateAdministratorDetails** umożliwia utworzenie obiektu szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="841b1-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="841b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="841b1-107">EXAMPLES</span></span>

### <span data-ttu-id="841b1-108">Przykład 1: Tworzenie obiektu szczegółów administratora certyfikatów</span><span class="sxs-lookup"><span data-stu-id="841b1-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="841b1-109">To polecenie powoduje utworzenie obiektu szczegółów administratora certyfikatu w pamięci, a następnie zapisanie go w zmiennej $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="841b1-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="841b1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="841b1-110">PARAMETERS</span></span>

### <span data-ttu-id="841b1-111">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="841b1-111">-EmailAddress</span></span>
<span data-ttu-id="841b1-112">Określa adres e-mail administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="841b1-112">Specifies the email address for the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="841b1-113">-FirstName</span><span class="sxs-lookup"><span data-stu-id="841b1-113">-FirstName</span></span>
<span data-ttu-id="841b1-114">Określa imię administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="841b1-114">Specifies the first name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="841b1-115">-LastName</span><span class="sxs-lookup"><span data-stu-id="841b1-115">-LastName</span></span>
<span data-ttu-id="841b1-116">Określa ostatnią nazwę administratora certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="841b1-116">Specifies the last name of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="841b1-117">-Rachunek</span><span class="sxs-lookup"><span data-stu-id="841b1-117">-PhoneNumber</span></span>
<span data-ttu-id="841b1-118">Określa numer telefonu administratora certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="841b1-118">Specifies the phone number of the certificate administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="841b1-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="841b1-119">-Confirm</span></span>
<span data-ttu-id="841b1-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="841b1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="841b1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="841b1-121">-WhatIf</span></span>
<span data-ttu-id="841b1-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="841b1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="841b1-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="841b1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="841b1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="841b1-124">-DefaultProfile</span></span>
<span data-ttu-id="841b1-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="841b1-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="841b1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="841b1-126">CommonParameters</span></span>
<span data-ttu-id="841b1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="841b1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="841b1-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="841b1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="841b1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="841b1-129">INPUTS</span></span>

## <span data-ttu-id="841b1-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="841b1-130">OUTPUTS</span></span>

### <span data-ttu-id="841b1-131">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="841b1-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="841b1-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="841b1-132">NOTES</span></span>

## <span data-ttu-id="841b1-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="841b1-133">RELATED LINKS</span></span>

[<span data-ttu-id="841b1-134">Nowe — AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="841b1-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

