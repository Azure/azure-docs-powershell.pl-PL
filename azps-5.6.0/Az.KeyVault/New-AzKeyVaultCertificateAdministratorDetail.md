---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: e72729b1721fb31ca2ce3a52d33f0295c55bb537
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001370"
---
# <span data-ttu-id="91bca-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="91bca-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="91bca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91bca-102">SYNOPSIS</span></span>
<span data-ttu-id="91bca-103">Tworzy obiekt szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="91bca-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="91bca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91bca-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91bca-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="91bca-105">DESCRIPTION</span></span>
<span data-ttu-id="91bca-106">Polecenie **cmdlet New-AzKeyVaultCertificateAdministratorDetail** tworzy obiekt szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="91bca-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="91bca-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91bca-107">EXAMPLES</span></span>

### <span data-ttu-id="91bca-108">Przykład 1. Tworzenie obiektu szczegółów administratora certyfikatu</span><span class="sxs-lookup"><span data-stu-id="91bca-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="91bca-109">To polecenie tworzy obiekt szczegółów administratora certyfikatu w pamięci, a następnie zapisuje go w $AdminDetails danych.</span><span class="sxs-lookup"><span data-stu-id="91bca-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="91bca-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91bca-110">PARAMETERS</span></span>

### <span data-ttu-id="91bca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91bca-111">-DefaultProfile</span></span>
<span data-ttu-id="91bca-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="91bca-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="91bca-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="91bca-113">-EmailAddress</span></span>
<span data-ttu-id="91bca-114">Określa adres e-mail administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="91bca-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="91bca-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="91bca-115">-FirstName</span></span>
<span data-ttu-id="91bca-116">Określa pierwszą nazwę administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="91bca-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="91bca-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="91bca-117">-LastName</span></span>
<span data-ttu-id="91bca-118">Określa nazwisko administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="91bca-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="91bca-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="91bca-119">-PhoneNumber</span></span>
<span data-ttu-id="91bca-120">Określa numer telefonu administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="91bca-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="91bca-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91bca-121">-Confirm</span></span>
<span data-ttu-id="91bca-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="91bca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91bca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91bca-123">-WhatIf</span></span>
<span data-ttu-id="91bca-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91bca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91bca-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="91bca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91bca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91bca-126">CommonParameters</span></span>
<span data-ttu-id="91bca-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91bca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91bca-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91bca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91bca-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91bca-129">INPUTS</span></span>

### <span data-ttu-id="91bca-130">System.String</span><span class="sxs-lookup"><span data-stu-id="91bca-130">System.String</span></span>

## <span data-ttu-id="91bca-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91bca-131">OUTPUTS</span></span>

### <span data-ttu-id="91bca-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="91bca-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="91bca-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91bca-133">NOTES</span></span>

## <span data-ttu-id="91bca-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91bca-134">RELATED LINKS</span></span>

[<span data-ttu-id="91bca-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="91bca-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

