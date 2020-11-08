---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050116"
---
# <span data-ttu-id="25194-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="25194-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="25194-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25194-102">SYNOPSIS</span></span>
<span data-ttu-id="25194-103">Umożliwia dodanie kontaktu do powiadomień o certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="25194-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="25194-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25194-104">SYNTAX</span></span>

### <span data-ttu-id="25194-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="25194-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25194-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="25194-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25194-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="25194-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25194-108">Opis</span><span class="sxs-lookup"><span data-stu-id="25194-108">DESCRIPTION</span></span>
<span data-ttu-id="25194-109">Polecenie cmdlet **Add-AzKeyVaultCertificateContact** umożliwia dodanie kontaktu dla magazynu kluczy na potrzeby powiadomień o certyfikatach w magazynie kluczy Azure.</span><span class="sxs-lookup"><span data-stu-id="25194-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="25194-110">Kontakt będzie otrzymywać aktualizacje dotyczące zdarzeń, takich jak certyfikat bliski wygaśnięcia, odnowienia certyfikatu itd.</span><span class="sxs-lookup"><span data-stu-id="25194-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="25194-111">Te zdarzenia są określone przez zasady certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="25194-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="25194-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25194-112">EXAMPLES</span></span>

### <span data-ttu-id="25194-113">Przykład 1: Dodawanie kontaktu z certyfikatem magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="25194-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="25194-114">To polecenie dodaje Patti jako kontakt certyfikatu dla magazynu kluczy ContosoKV01 i zwraca listę kontaktów magazynu "ContosoKV01".</span><span class="sxs-lookup"><span data-stu-id="25194-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="25194-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25194-115">PARAMETERS</span></span>

### <span data-ttu-id="25194-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25194-116">-DefaultProfile</span></span>
<span data-ttu-id="25194-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="25194-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25194-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="25194-118">-EmailAddress</span></span>
<span data-ttu-id="25194-119">Określa adres e-mail kontaktu.</span><span class="sxs-lookup"><span data-stu-id="25194-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="25194-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="25194-120">-InputObject</span></span>
<span data-ttu-id="25194-121">Obiekt magazynu.</span><span class="sxs-lookup"><span data-stu-id="25194-121">KeyVault object.</span></span>

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

### <span data-ttu-id="25194-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25194-122">-PassThru</span></span>
<span data-ttu-id="25194-123">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="25194-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25194-124">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="25194-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25194-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25194-125">-ResourceId</span></span>
<span data-ttu-id="25194-126">Identyfikator zasobu magazynu.</span><span class="sxs-lookup"><span data-stu-id="25194-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="25194-127">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="25194-127">-VaultName</span></span>
<span data-ttu-id="25194-128">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="25194-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="25194-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25194-129">-Confirm</span></span>
<span data-ttu-id="25194-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25194-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25194-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25194-131">-WhatIf</span></span>
<span data-ttu-id="25194-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25194-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25194-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25194-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25194-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25194-134">CommonParameters</span></span>
<span data-ttu-id="25194-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25194-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25194-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25194-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25194-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25194-137">INPUTS</span></span>

### <span data-ttu-id="25194-138">Microsoft. Azure. Commands. platforming. models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="25194-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="25194-139">System. String</span><span class="sxs-lookup"><span data-stu-id="25194-139">System.String</span></span>

## <span data-ttu-id="25194-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25194-140">OUTPUTS</span></span>

### <span data-ttu-id="25194-141">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="25194-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="25194-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25194-142">NOTES</span></span>

## <span data-ttu-id="25194-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25194-143">RELATED LINKS</span></span>

[<span data-ttu-id="25194-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="25194-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="25194-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="25194-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

