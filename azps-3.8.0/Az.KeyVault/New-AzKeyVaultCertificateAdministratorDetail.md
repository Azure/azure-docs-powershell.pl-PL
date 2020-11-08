---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049650"
---
# <span data-ttu-id="4c5db-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="4c5db-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="4c5db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c5db-102">SYNOPSIS</span></span>
<span data-ttu-id="4c5db-103">Tworzy obiekt szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="4c5db-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="4c5db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c5db-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c5db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c5db-105">DESCRIPTION</span></span>
<span data-ttu-id="4c5db-106">Polecenie cmdlet **New-AzKeyVaultCertificateAdministratorDetail** umożliwia utworzenie obiektu szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="4c5db-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="4c5db-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c5db-107">EXAMPLES</span></span>

### <span data-ttu-id="4c5db-108">Przykład 1: Tworzenie obiektu szczegółów administratora certyfikatów</span><span class="sxs-lookup"><span data-stu-id="4c5db-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="4c5db-109">To polecenie powoduje utworzenie obiektu szczegółów administratora certyfikatu w pamięci, a następnie zapisanie go w zmiennej $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="4c5db-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="4c5db-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c5db-110">PARAMETERS</span></span>

### <span data-ttu-id="4c5db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c5db-111">-DefaultProfile</span></span>
<span data-ttu-id="4c5db-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4c5db-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c5db-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="4c5db-113">-EmailAddress</span></span>
<span data-ttu-id="4c5db-114">Określa adres e-mail administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="4c5db-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="4c5db-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="4c5db-115">-FirstName</span></span>
<span data-ttu-id="4c5db-116">Określa imię administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="4c5db-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="4c5db-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="4c5db-117">-LastName</span></span>
<span data-ttu-id="4c5db-118">Określa ostatnią nazwę administratora certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="4c5db-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="4c5db-119">-Rachunek</span><span class="sxs-lookup"><span data-stu-id="4c5db-119">-PhoneNumber</span></span>
<span data-ttu-id="4c5db-120">Określa numer telefonu administratora certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="4c5db-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="4c5db-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c5db-121">-Confirm</span></span>
<span data-ttu-id="4c5db-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c5db-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c5db-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c5db-123">-WhatIf</span></span>
<span data-ttu-id="4c5db-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c5db-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c5db-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c5db-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c5db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c5db-126">CommonParameters</span></span>
<span data-ttu-id="4c5db-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c5db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c5db-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c5db-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c5db-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c5db-129">INPUTS</span></span>

### <span data-ttu-id="4c5db-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4c5db-130">System.String</span></span>

## <span data-ttu-id="4c5db-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c5db-131">OUTPUTS</span></span>

### <span data-ttu-id="4c5db-132">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="4c5db-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="4c5db-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c5db-133">NOTES</span></span>

## <span data-ttu-id="4c5db-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c5db-134">RELATED LINKS</span></span>

[<span data-ttu-id="4c5db-135">Nowe — AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="4c5db-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

