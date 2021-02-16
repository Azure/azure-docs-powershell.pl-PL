---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 775AB0E8-EC3C-4F96-8AF8-51C1DFEEF082
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultcertificateadministratordetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultCertificateAdministratorDetail.md
ms.openlocfilehash: 39deb08468912bf727198ec4f90f5f4f0680941f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200018"
---
# <span data-ttu-id="485b3-101">New-AzKeyVaultCertificateAdministratorDetail</span><span class="sxs-lookup"><span data-stu-id="485b3-101">New-AzKeyVaultCertificateAdministratorDetail</span></span>

## <span data-ttu-id="485b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="485b3-102">SYNOPSIS</span></span>
<span data-ttu-id="485b3-103">Tworzy obiekt szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="485b3-103">Creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="485b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="485b3-104">SYNTAX</span></span>

```
New-AzKeyVaultCertificateAdministratorDetail [-FirstName <String>] [-LastName <String>]
 [-EmailAddress <String>] [-PhoneNumber <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="485b3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="485b3-105">DESCRIPTION</span></span>
<span data-ttu-id="485b3-106">Polecenie **cmdlet New-AzKeyVaultCertificateAdministratorDetail** tworzy obiekt szczegółów administratora certyfikatu w pamięci.</span><span class="sxs-lookup"><span data-stu-id="485b3-106">The **New-AzKeyVaultCertificateAdministratorDetail** cmdlet creates an in-memory certificate administrator details object.</span></span>

## <span data-ttu-id="485b3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="485b3-107">EXAMPLES</span></span>

### <span data-ttu-id="485b3-108">Przykład 1. Tworzenie obiektu szczegółów administratora certyfikatu</span><span class="sxs-lookup"><span data-stu-id="485b3-108">Example 1: Create a certificate administrator details object</span></span>
```
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName "Patti" -LastName "Fuller" -EmailAddress "patti.fuller@contoso.com" -PhoneNumber "5553334444"
PS C:\> $AdminDetails

FirstName LastName EmailAddress             PhoneNumber
--------- -------- ------------             -----------
Patti     Fuller   patti.fuller@contoso.com 5553334444
```

<span data-ttu-id="485b3-109">To polecenie tworzy obiekt szczegółów administratora certyfikatu w pamięci, a następnie zapisuje go w $AdminDetails danych.</span><span class="sxs-lookup"><span data-stu-id="485b3-109">This command creates an in-memory certificate administrator details object, and then stores it in the $AdminDetails variable.</span></span>

## <span data-ttu-id="485b3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="485b3-110">PARAMETERS</span></span>

### <span data-ttu-id="485b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="485b3-111">-DefaultProfile</span></span>
<span data-ttu-id="485b3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="485b3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="485b3-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="485b3-113">-EmailAddress</span></span>
<span data-ttu-id="485b3-114">Określa adres e-mail administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="485b3-114">Specifies the email address for the certificate administrator.</span></span>

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

### <span data-ttu-id="485b3-115">-FirstName</span><span class="sxs-lookup"><span data-stu-id="485b3-115">-FirstName</span></span>
<span data-ttu-id="485b3-116">Określa pierwszą nazwę administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="485b3-116">Specifies the first name of the certificate administrator.</span></span>

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

### <span data-ttu-id="485b3-117">-LastName</span><span class="sxs-lookup"><span data-stu-id="485b3-117">-LastName</span></span>
<span data-ttu-id="485b3-118">Określa nazwisko administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="485b3-118">Specifies the last name of the certificate administrator.</span></span>

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

### <span data-ttu-id="485b3-119">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="485b3-119">-PhoneNumber</span></span>
<span data-ttu-id="485b3-120">Określa numer telefonu administratora certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="485b3-120">Specifies the phone number of the certificate administrator.</span></span>

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

### <span data-ttu-id="485b3-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="485b3-121">-Confirm</span></span>
<span data-ttu-id="485b3-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="485b3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="485b3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="485b3-123">-WhatIf</span></span>
<span data-ttu-id="485b3-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="485b3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="485b3-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="485b3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="485b3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="485b3-126">CommonParameters</span></span>
<span data-ttu-id="485b3-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="485b3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="485b3-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="485b3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="485b3-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="485b3-129">INPUTS</span></span>

### <span data-ttu-id="485b3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="485b3-130">System.String</span></span>

## <span data-ttu-id="485b3-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="485b3-131">OUTPUTS</span></span>

### <span data-ttu-id="485b3-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span><span class="sxs-lookup"><span data-stu-id="485b3-132">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateAdministratorDetails</span></span>

## <span data-ttu-id="485b3-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="485b3-133">NOTES</span></span>

## <span data-ttu-id="485b3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="485b3-134">RELATED LINKS</span></span>

[<span data-ttu-id="485b3-135">New-AzKeyVaultCertificateOrganizationDetail</span><span class="sxs-lookup"><span data-stu-id="485b3-135">New-AzKeyVaultCertificateOrganizationDetail</span></span>](./New-AzKeyVaultCertificateOrganizationDetail.md)

