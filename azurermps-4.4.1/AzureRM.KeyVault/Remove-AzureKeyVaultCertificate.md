---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 9a33d4efdd82ad03b94ea9a7e862fb5e13eb30d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553854"
---
# <span data-ttu-id="97410-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="97410-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="97410-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97410-102">SYNOPSIS</span></span>
<span data-ttu-id="97410-103">Usuwa certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="97410-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97410-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97410-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97410-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97410-105">DESCRIPTION</span></span>
<span data-ttu-id="97410-106">Polecenie cmdlet **Remove-AzureKeyVaultCertificate** usuwa certyfikat z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="97410-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="97410-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97410-107">EXAMPLES</span></span>

### <span data-ttu-id="97410-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="97410-108">Example 1: Remove a certificate</span></span>
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

<span data-ttu-id="97410-109">To polecenie usuwa certyfikat o nazwie SelfSigned01 z magazynu kluczy o nazwie ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="97410-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="97410-110">To polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="97410-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="97410-111">Dlatego polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="97410-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="97410-112">Przykład 3: trwałe przeczyszczanie usuniętego certyfikatu z magazynu kluczy</span><span class="sxs-lookup"><span data-stu-id="97410-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="97410-113">To polecenie powoduje trwałe usunięcie certyfikatu o nazwie "Moje CERT" z magazynu kluczy o nazwie "contoso".</span><span class="sxs-lookup"><span data-stu-id="97410-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="97410-114">Wykonanie tego polecenia cmdlet wymaga uprawnienia "Wyczyść", które musi być wcześniej i wyraźnie udzielone użytkownikowi w tym magazynie kluczy.</span><span class="sxs-lookup"><span data-stu-id="97410-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="97410-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97410-115">PARAMETERS</span></span>

### <span data-ttu-id="97410-116">-Force</span><span class="sxs-lookup"><span data-stu-id="97410-116">-Force</span></span>
<span data-ttu-id="97410-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="97410-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="97410-118">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="97410-118">-InRemovedState</span></span>
<span data-ttu-id="97410-119">Jeśli ta operacja jest obecna, usuwa już trwale usunięty certyfikat.</span><span class="sxs-lookup"><span data-stu-id="97410-119">If present, removes the previously deleted certificate permanently.</span></span>

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

### <span data-ttu-id="97410-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="97410-120">-Name</span></span>
<span data-ttu-id="97410-121">Określa nazwę certyfikatu usuniętego przez ten aplet polecenia z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="97410-121">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="97410-122">To polecenie cmdlet konstruuje w pełni kwalifikowaną nazwę domeny (FQDN) certyfikatu na podstawie nazwy, jaką określa ten parametr, nazwy magazynu kluczy i bieżącego środowiska.</span><span class="sxs-lookup"><span data-stu-id="97410-122">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97410-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97410-123">-PassThru</span></span>
<span data-ttu-id="97410-124">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="97410-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="97410-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="97410-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="97410-126">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="97410-126">-VaultName</span></span>
<span data-ttu-id="97410-127">Określa nazwę magazynu kluczy, z którego to polecenie cmdlet usuwa certyfikat.</span><span class="sxs-lookup"><span data-stu-id="97410-127">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="97410-128">To polecenie cmdlet konstruuje nazwę FQDN magazynu kluczy na podstawie nazwy, jaką ten parametr określa i bieżące środowisko.</span><span class="sxs-lookup"><span data-stu-id="97410-128">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97410-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="97410-129">-Confirm</span></span>
<span data-ttu-id="97410-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97410-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97410-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97410-131">-WhatIf</span></span>
<span data-ttu-id="97410-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97410-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97410-133">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97410-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97410-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="97410-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97410-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97410-135">-DefaultProfile</span></span>
<span data-ttu-id="97410-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="97410-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97410-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97410-137">CommonParameters</span></span>
<span data-ttu-id="97410-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97410-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97410-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97410-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97410-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97410-140">INPUTS</span></span>

## <span data-ttu-id="97410-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97410-141">OUTPUTS</span></span>

### <span data-ttu-id="97410-142">Microsoft. Azure. Commands. platforming. models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="97410-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="97410-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97410-143">NOTES</span></span>

## <span data-ttu-id="97410-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97410-144">RELATED LINKS</span></span>

[<span data-ttu-id="97410-145">Dodaj-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="97410-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="97410-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="97410-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="97410-147">Import — AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="97410-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="97410-148">Cofanie — AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="97410-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
