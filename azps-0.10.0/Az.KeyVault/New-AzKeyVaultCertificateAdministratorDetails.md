---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/new-AzKeyvaultcertificateadministratordetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetails.md
ms.openlocfilehash: 6844a8f4858452a1ebf9df306d75e495603703aa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891285"
---
# <span data-ttu-id="f2a8d-101">New-AzKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="f2a8d-101">New-AzKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="f2a8d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2a8d-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a8d-103">Tworzy obiekt szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="f2a8d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2a8d-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetails [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2a8d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2a8d-105">DESCRIPTION</span></span>
<span data-ttu-id="f2a8d-106">Polecenie cmdlet **New-AzKeyVaultCertificateAdministratorDetails** umożliwia utworzenie obiektu szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-106">The **New-AzKeyVaultCertificateAdministratorDetails** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="f2a8d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2a8d-107">EXAMPLES</span></span>

### <span data-ttu-id="f2a8d-108">Przykład 1: Tworzenie obiektu szczegółów administratora certyfikatów</span><span class="sxs-lookup"><span data-stu-id="f2a8d-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\>$AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
```

<span data-ttu-id="f2a8d-109">To polecenie powoduje utworzenie obiektu szczegółów administratora certyfikatu w pamięci, a następnie zapisanie go w zmiennej $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="f2a8d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2a8d-110">PARAMETERS</span></span>

### <span data-ttu-id="f2a8d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a8d-111">-DefaultProfile</span></span>
<span data-ttu-id="f2a8d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f2a8d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2a8d-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="f2a8d-113">-EmailAddress</span></span>
<span data-ttu-id="f2a8d-114">Określa adres e-mail administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="f2a8d-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="f2a8d-115">-FirstName</span></span>
<span data-ttu-id="f2a8d-116">Określa imię administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="f2a8d-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="f2a8d-117">-LastName</span></span>
<span data-ttu-id="f2a8d-118">Określa ostatnią nazwę administratora certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="f2a8d-119">-Rachunek</span><span class="sxs-lookup"><span data-stu-id="f2a8d-119">-PhoneNumber</span></span>
<span data-ttu-id="f2a8d-120">Określa numer telefonu administratora certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="f2a8d-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2a8d-121">-Confirm</span></span>
<span data-ttu-id="f2a8d-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2a8d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2a8d-123">-WhatIf</span></span>
<span data-ttu-id="f2a8d-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2a8d-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2a8d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a8d-126">CommonParameters</span></span>
<span data-ttu-id="f2a8d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a8d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2a8d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a8d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2a8d-129">INPUTS</span></span>

### <span data-ttu-id="f2a8d-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f2a8d-130">None</span></span>
<span data-ttu-id="f2a8d-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f2a8d-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f2a8d-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2a8d-132">OUTPUTS</span></span>

### <span data-ttu-id="f2a8d-133">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="f2a8d-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="f2a8d-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2a8d-134">NOTES</span></span>

## <span data-ttu-id="f2a8d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2a8d-135">RELATED LINKS</span></span>

[<span data-ttu-id="f2a8d-136">Nowe — AzKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="f2a8d-136">New-AzKeyVaultCertificateOrganizationDetails</span></span>](./New-AzKeyVaultCertificateOrganizationDetails.md)

