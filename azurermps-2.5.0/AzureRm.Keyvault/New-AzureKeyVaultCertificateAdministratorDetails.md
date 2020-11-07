---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/new-azurekeyvaultcertificateadministratordetails
schema: 2.0.0
ms.openlocfilehash: 50da8cae0af437ee86fd7462b285b812368b2508
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898914"
---
# <span data-ttu-id="29998-101">New-AzureKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="29998-101">New-AzureKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="29998-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29998-102">SYNOPSIS</span></span>
<span data-ttu-id="29998-103">Tworzy obiekt szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="29998-103">Creates an in-memory certificate administrator details object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29998-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29998-104">SYNTAX</span></span>

```
New-AzureKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29998-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29998-105">DESCRIPTION</span></span>
<span data-ttu-id="29998-106">Polecenie cmdlet **New-AzureKeyVaultCertificateAdministratorDetails** umożliwia utworzenie obiektu szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="29998-106">The **New-AzureKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="29998-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29998-107">EXAMPLES</span></span>

### <span data-ttu-id="29998-108">Przykład 1: Tworzenie obiektu szczegółów administratora certyfikatów</span><span class="sxs-lookup"><span data-stu-id="29998-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="29998-109">To polecenie powoduje utworzenie obiektu szczegółów administratora certyfikatu w pamięci, a następnie zapisanie go w zmiennej $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="29998-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="29998-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29998-110">PARAMETERS</span></span>

### <span data-ttu-id="29998-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29998-111">-DefaultProfile</span></span>
<span data-ttu-id="29998-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="29998-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29998-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="29998-113">-EmailAddress</span></span>
<span data-ttu-id="29998-114">Określa adres e-mail administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="29998-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="29998-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="29998-115">-FirstName</span></span>
<span data-ttu-id="29998-116">Określa imię administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="29998-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="29998-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="29998-117">-LastName</span></span>
<span data-ttu-id="29998-118">Określa ostatnią nazwę administratora certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="29998-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="29998-119">-Rachunek</span><span class="sxs-lookup"><span data-stu-id="29998-119">-PhoneNumber</span></span>
<span data-ttu-id="29998-120">Określa numer telefonu administratora certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="29998-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="29998-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29998-121">-Confirm</span></span>
<span data-ttu-id="29998-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29998-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29998-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29998-123">-WhatIf</span></span>
<span data-ttu-id="29998-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29998-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29998-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29998-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29998-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29998-126">CommonParameters</span></span>
<span data-ttu-id="29998-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29998-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29998-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29998-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29998-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29998-129">INPUTS</span></span>

## <span data-ttu-id="29998-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29998-130">OUTPUTS</span></span>

### <span data-ttu-id="29998-131">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="29998-131">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="29998-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29998-132">NOTES</span></span>

## <span data-ttu-id="29998-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29998-133">RELATED LINKS</span></span>

[<span data-ttu-id="29998-134">Nowe — AzureKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="29998-134">New-AzureKeyVaultCertificateOrganizationDetails</span></span>](./New-AzureKeyVaultCertificateOrganizationDetails.md)

