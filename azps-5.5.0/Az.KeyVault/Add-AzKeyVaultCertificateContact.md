---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203872"
---
# <span data-ttu-id="16829-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="16829-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="16829-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16829-102">SYNOPSIS</span></span>
<span data-ttu-id="16829-103">Dodaje kontakt do powiadomień o certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="16829-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="16829-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16829-104">SYNTAX</span></span>

### <span data-ttu-id="16829-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="16829-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16829-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="16829-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16829-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="16829-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16829-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="16829-108">DESCRIPTION</span></span>
<span data-ttu-id="16829-109">Polecenie **cmdlet Add-AzKeyVaultCertificateContact** dodaje kontakt dla magazynu kluczy dla powiadomień o certyfikatach w magazynie kluczy platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="16829-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="16829-110">Kontakt otrzymuje aktualizacje dotyczące takich zdarzeń, jak certyfikat bliski wygaśnięcia, odnowienie certyfikatu itp.</span><span class="sxs-lookup"><span data-stu-id="16829-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="16829-111">Te zdarzenia są określane przez zasady certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="16829-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="16829-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16829-112">EXAMPLES</span></span>

### <span data-ttu-id="16829-113">Przykład 1. Dodawanie kontaktu certyfikatu magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="16829-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="16829-114">To polecenie dodaje Patti Fuller jako kontakt certyfikatu dla magazynu kluczy ContosoKV01 i zwraca listę kontaktów dla magazynu "ContosoKV01".</span><span class="sxs-lookup"><span data-stu-id="16829-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="16829-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16829-115">PARAMETERS</span></span>

### <span data-ttu-id="16829-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16829-116">-DefaultProfile</span></span>
<span data-ttu-id="16829-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="16829-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16829-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="16829-118">-EmailAddress</span></span>
<span data-ttu-id="16829-119">Określa adres e-mail kontaktu.</span><span class="sxs-lookup"><span data-stu-id="16829-119">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16829-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="16829-120">-InputObject</span></span>
<span data-ttu-id="16829-121">Obiekt KeyVault.</span><span class="sxs-lookup"><span data-stu-id="16829-121">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16829-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16829-122">-PassThru</span></span>
<span data-ttu-id="16829-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="16829-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="16829-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="16829-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16829-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="16829-125">-ResourceId</span></span>
<span data-ttu-id="16829-126">Identyfikator zasobu KeyVault.</span><span class="sxs-lookup"><span data-stu-id="16829-126">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16829-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="16829-127">-VaultName</span></span>
<span data-ttu-id="16829-128">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="16829-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16829-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16829-129">-Confirm</span></span>
<span data-ttu-id="16829-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="16829-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16829-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16829-131">-WhatIf</span></span>
<span data-ttu-id="16829-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16829-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16829-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="16829-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16829-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16829-134">CommonParameters</span></span>
<span data-ttu-id="16829-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16829-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16829-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16829-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16829-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16829-137">INPUTS</span></span>

### <span data-ttu-id="16829-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="16829-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="16829-139">System.String</span><span class="sxs-lookup"><span data-stu-id="16829-139">System.String</span></span>

## <span data-ttu-id="16829-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16829-140">OUTPUTS</span></span>

### <span data-ttu-id="16829-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="16829-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="16829-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16829-142">NOTES</span></span>

## <span data-ttu-id="16829-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16829-143">RELATED LINKS</span></span>

[<span data-ttu-id="16829-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="16829-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="16829-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="16829-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

