---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ff363ae1bf6581baaeb177edd4e215494c82f85f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868035"
---
# <span data-ttu-id="b142a-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b142a-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="b142a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b142a-102">SYNOPSIS</span></span>
<span data-ttu-id="b142a-103">Umożliwia dodanie kontaktu do powiadomień o certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="b142a-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="b142a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b142a-104">SYNTAX</span></span>

### <span data-ttu-id="b142a-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b142a-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b142a-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="b142a-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b142a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b142a-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b142a-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b142a-108">DESCRIPTION</span></span>
<span data-ttu-id="b142a-109">Polecenie cmdlet **Add-AzKeyVaultCertificateContact** umożliwia dodanie kontaktu dla magazynu kluczy na potrzeby powiadomień o certyfikatach w magazynie kluczy Azure.</span><span class="sxs-lookup"><span data-stu-id="b142a-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="b142a-110">Kontakt będzie otrzymywać aktualizacje dotyczące zdarzeń, takich jak certyfikat bliski wygaśnięcia, odnowienia certyfikatu itd.</span><span class="sxs-lookup"><span data-stu-id="b142a-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="b142a-111">Te zdarzenia są określone przez zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="b142a-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="b142a-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b142a-112">EXAMPLES</span></span>

### <span data-ttu-id="b142a-113">Przykład 1: Dodawanie kontaktu z certyfikatem magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="b142a-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="b142a-114">To polecenie dodaje Patti jako kontakt certyfikatu dla magazynu kluczy ContosoKV01 i zwraca listę kontaktów magazynu "ContosoKV01".</span><span class="sxs-lookup"><span data-stu-id="b142a-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="b142a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b142a-115">PARAMETERS</span></span>

### <span data-ttu-id="b142a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b142a-116">-DefaultProfile</span></span>
<span data-ttu-id="b142a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b142a-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b142a-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b142a-118">-EmailAddress</span></span>
<span data-ttu-id="b142a-119">Określa adres e-mail kontaktu.</span><span class="sxs-lookup"><span data-stu-id="b142a-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="b142a-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b142a-120">-InputObject</span></span>
<span data-ttu-id="b142a-121">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="b142a-121">KeyVault object.</span></span>

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

### <span data-ttu-id="b142a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b142a-122">-PassThru</span></span>
<span data-ttu-id="b142a-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b142a-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b142a-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b142a-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b142a-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b142a-125">-ResourceId</span></span>
<span data-ttu-id="b142a-126">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="b142a-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="b142a-127">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="b142a-127">-VaultName</span></span>
<span data-ttu-id="b142a-128">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b142a-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="b142a-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b142a-129">-Confirm</span></span>
<span data-ttu-id="b142a-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b142a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b142a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b142a-131">-WhatIf</span></span>
<span data-ttu-id="b142a-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b142a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b142a-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b142a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b142a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b142a-134">CommonParameters</span></span>
<span data-ttu-id="b142a-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b142a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b142a-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b142a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b142a-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b142a-137">INPUTS</span></span>

### <span data-ttu-id="b142a-138">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b142a-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b142a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b142a-139">System.String</span></span>

## <span data-ttu-id="b142a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b142a-140">OUTPUTS</span></span>

### <span data-ttu-id="b142a-141">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b142a-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="b142a-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b142a-142">NOTES</span></span>

## <span data-ttu-id="b142a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b142a-143">RELATED LINKS</span></span>

[<span data-ttu-id="b142a-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b142a-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="b142a-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b142a-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

