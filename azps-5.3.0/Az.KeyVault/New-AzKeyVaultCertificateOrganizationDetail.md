---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: 56b956aa8a65c4586859325f110f3ce593b2289c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499066"
---
# <span data-ttu-id="22f25-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="22f25-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="22f25-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22f25-102">SYNOPSIS</span></span>
<span data-ttu-id="22f25-103">Tworzy obiekt szczegółów organizacji certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="22f25-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="22f25-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22f25-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22f25-105">Opis</span><span class="sxs-lookup"><span data-stu-id="22f25-105">DESCRIPTION</span></span>
<span data-ttu-id="22f25-106">Polecenie cmdlet **New-AzKeyVaultCertificateOrganizationDetail** umożliwia utworzenie obiektu szczegółów organizacji certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="22f25-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="22f25-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22f25-107">EXAMPLES</span></span>

### <span data-ttu-id="22f25-108">Przykład 1: Tworzenie obiektu szczegółów organizacji</span><span class="sxs-lookup"><span data-stu-id="22f25-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="22f25-109">Pierwsze polecenie powoduje utworzenie obiektu szczegółów administratora certyfikatu, a następnie zapisanie go w zmiennej $AdminDetails.</span><span class="sxs-lookup"><span data-stu-id="22f25-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="22f25-110">Drugie polecenie tworzy obiekt szczegóły organizacji certyfikatu, a następnie zapisuje go w zmiennej $OrgDetails.</span><span class="sxs-lookup"><span data-stu-id="22f25-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="22f25-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22f25-111">PARAMETERS</span></span>

### <span data-ttu-id="22f25-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="22f25-112">-AdministratorDetails</span></span>
<span data-ttu-id="22f25-113">Określa administratorów organizacji certyfikacji.</span><span class="sxs-lookup"><span data-stu-id="22f25-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="22f25-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22f25-114">-DefaultProfile</span></span>
<span data-ttu-id="22f25-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="22f25-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22f25-116">-ID</span><span class="sxs-lookup"><span data-stu-id="22f25-116">-Id</span></span>
<span data-ttu-id="22f25-117">Określa identyfikator organizacji.</span><span class="sxs-lookup"><span data-stu-id="22f25-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="22f25-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22f25-118">-Confirm</span></span>
<span data-ttu-id="22f25-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22f25-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22f25-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22f25-120">-WhatIf</span></span>
<span data-ttu-id="22f25-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22f25-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22f25-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="22f25-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22f25-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22f25-123">CommonParameters</span></span>
<span data-ttu-id="22f25-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22f25-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22f25-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22f25-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22f25-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22f25-126">INPUTS</span></span>

### <span data-ttu-id="22f25-127">System. String</span><span class="sxs-lookup"><span data-stu-id="22f25-127">System.String</span></span>

### <span data-ttu-id="22f25-128">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. Commands. platform. PSKeyVaultCertificateAdministratorDetails, Microsoft. Azure. PowerShell. aplety. magazyny, wersja = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="22f25-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="22f25-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22f25-129">OUTPUTS</span></span>

### <span data-ttu-id="22f25-130">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="22f25-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="22f25-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22f25-131">NOTES</span></span>

## <span data-ttu-id="22f25-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22f25-132">RELATED LINKS</span></span>

[<span data-ttu-id="22f25-133">Nowe — AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="22f25-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

