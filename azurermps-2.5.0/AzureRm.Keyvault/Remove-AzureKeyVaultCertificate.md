---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 662304cff991da0d9ffe9d946e63bc94ba51e4a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897394"
---
# <span data-ttu-id="c4104-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c4104-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="c4104-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4104-102">SYNOPSIS</span></span>
<span data-ttu-id="c4104-103">Usuwa certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="c4104-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4104-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4104-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4104-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c4104-105">DESCRIPTION</span></span>
<span data-ttu-id="c4104-106">Polecenie cmdlet **Remove-AzureKeyVaultCertificate** usuwa certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="c4104-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="c4104-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4104-107">EXAMPLES</span></span>

### <span data-ttu-id="c4104-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="c4104-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="c4104-109">To polecenie usuwa certyfikat o nazwie SelfSigned01 z magazynu kluczy o nazwie ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="c4104-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="c4104-110">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="c4104-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c4104-111">Dlatego polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c4104-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="c4104-112">Przykład 3: trwałe przeczyszczanie usuniętego certyfikatu z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="c4104-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="c4104-113">To polecenie powoduje trwałe usunięcie certyfikatu o nazwie "Moje CERT" z magazynu kluczy o nazwie "contoso".</span><span class="sxs-lookup"><span data-stu-id="c4104-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="c4104-114">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi w tym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="c4104-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="c4104-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4104-115">PARAMETERS</span></span>

### <span data-ttu-id="c4104-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4104-116">-DefaultProfile</span></span>
<span data-ttu-id="c4104-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c4104-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4104-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c4104-118">-Force</span></span>
<span data-ttu-id="c4104-119">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c4104-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4104-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c4104-120">-InRemovedState</span></span>
<span data-ttu-id="c4104-121">Jeśli ta operacja jest obecna, usuwa już trwale usunięty certyfikat</span><span class="sxs-lookup"><span data-stu-id="c4104-121">If present, removes the previously deleted certificate permanently</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4104-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c4104-122">-Name</span></span>
<span data-ttu-id="c4104-123">Określa nazwę certyfikatu usuniętego przez ten aplet polecenia z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="c4104-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="c4104-124">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) certyfikatu na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="c4104-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4104-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4104-125">-PassThru</span></span>
<span data-ttu-id="c4104-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c4104-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c4104-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c4104-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4104-128">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="c4104-128">-VaultName</span></span>
<span data-ttu-id="c4104-129">Określa nazwę magazynu kluczy, z którego to polecenie cmdlet usuwa certyfikat.</span><span class="sxs-lookup"><span data-stu-id="c4104-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="c4104-130">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="c4104-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4104-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4104-131">-Confirm</span></span>
<span data-ttu-id="c4104-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4104-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4104-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4104-133">-WhatIf</span></span>
<span data-ttu-id="c4104-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4104-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4104-135">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4104-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4104-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4104-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4104-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4104-137">CommonParameters</span></span>
<span data-ttu-id="c4104-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4104-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4104-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4104-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4104-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4104-140">INPUTS</span></span>

## <span data-ttu-id="c4104-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4104-141">OUTPUTS</span></span>

### <span data-ttu-id="c4104-142">Microsoft. Azure. Commands. platforming. models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="c4104-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="c4104-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4104-143">NOTES</span></span>

## <span data-ttu-id="c4104-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4104-144">RELATED LINKS</span></span>

[<span data-ttu-id="c4104-145">Dodaj-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c4104-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="c4104-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c4104-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="c4104-147">Import — AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c4104-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="c4104-148">Cofanie — AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="c4104-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
