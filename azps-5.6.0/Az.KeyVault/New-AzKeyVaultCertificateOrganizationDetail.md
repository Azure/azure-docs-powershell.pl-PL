---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 0E1C05B0-8CF6-4C03-AA05-B13A4059A280
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificateorganizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateOrganizationDetail.md
ms.openlocfilehash: ee2be43882eb434d8bbc533e0d10722f63427a83
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001345"
---
# <span data-ttu-id="a14d4-101">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="a14d4-101">New-AzKeyVaultCertificateOrganizationDetail</span></span>

## <span data-ttu-id="a14d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a14d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a14d4-103">Tworzy obiekt szczegółów organizacji certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="a14d4-103">Creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="a14d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a14d4-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateOrganizationDetail [-Id <String>]
 [-AdministratorDetails <System.Collections.Generic.List`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a14d4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a14d4-105">DESCRIPTION</span></span>
<span data-ttu-id="a14d4-106">Polecenie **cmdlet New-AzKeyVaultCertificateOrganizationDetail** tworzy obiekt szczegółów organizacji certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="a14d4-106">The **New-AzKeyVaultCertificateOrganizationDetail** cmdlet creates an in-memory certificate organization details object.</span></span>

## <span data-ttu-id="a14d4-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a14d4-107">EXAMPLES</span></span>

### <span data-ttu-id="a14d4-108">Przykład 1. Tworzenie obiektu szczegółów organizacji</span><span class="sxs-lookup"><span data-stu-id="a14d4-108">Example 1: Create an organization details object</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "Patti.Fuller@contoso.com" -PhoneNumber "1234567890"
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails

Id AdministratorDetails
-- --------------------
   {Patti}
```

<span data-ttu-id="a14d4-109">Pierwsze polecenie tworzy obiekt szczegółów administratora certyfikatu, a następnie zapisuje go w $AdminDetails certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a14d4-109">The first command creates a certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>
<span data-ttu-id="a14d4-110">Drugie polecenie tworzy obiekt szczegółów organizacji certyfikatu, a następnie zapisuje go w $OrgDetails danych.</span><span class="sxs-lookup"><span data-stu-id="a14d4-110">The second command creates a certificate organization details object, and then stores it in the $OrgDetails variable.</span></span>

## <span data-ttu-id="a14d4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a14d4-111">PARAMETERS</span></span>

### <span data-ttu-id="a14d4-112">-AdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="a14d4-112">-AdministratorDetails</span></span>
<span data-ttu-id="a14d4-113">Określa administratorów organizacji certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="a14d4-113">Specifies the certificate organization administrators.</span></span>

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

### <span data-ttu-id="a14d4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a14d4-114">-DefaultProfile</span></span>
<span data-ttu-id="a14d4-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a14d4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a14d4-116">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="a14d4-116">-Id</span></span>
<span data-ttu-id="a14d4-117">Określa identyfikator organizacji.</span><span class="sxs-lookup"><span data-stu-id="a14d4-117">Specifies the identifier for the organization.</span></span>

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

### <span data-ttu-id="a14d4-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a14d4-118">-Confirm</span></span>
<span data-ttu-id="a14d4-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a14d4-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a14d4-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a14d4-120">-WhatIf</span></span>
<span data-ttu-id="a14d4-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a14d4-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a14d4-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a14d4-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a14d4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a14d4-123">CommonParameters</span></span>
<span data-ttu-id="a14d4-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a14d4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a14d4-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a14d4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a14d4-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a14d4-126">INPUTS</span></span>

### <span data-ttu-id="a14d4-127">System.String</span><span class="sxs-lookup"><span data-stu-id="a14d4-127">System.String</span></span>

### <span data-ttu-id="a14d4-128">System.Collections.generic.List'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlet.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="a14d4-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a14d4-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a14d4-129">OUTPUTS</span></span>

### <span data-ttu-id="a14d4-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="a14d4-130">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

## <span data-ttu-id="a14d4-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a14d4-131">NOTES</span></span>

## <span data-ttu-id="a14d4-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a14d4-132">RELATED LINKS</span></span>

[<span data-ttu-id="a14d4-133">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="a14d4-133">New-AzKeyVaultCertificateAdministratorDetail</span></span>](./New-AzKeyVaultCertificateAdministratorDetail.md)

