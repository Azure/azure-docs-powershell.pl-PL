---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 70d6d39ed3e2083bf0f52e9e56808b7d36f1cc24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544287"
---
# <span data-ttu-id="219bf-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="219bf-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="219bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="219bf-102">SYNOPSIS</span></span>
<span data-ttu-id="219bf-103">Usuwa operację certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="219bf-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="219bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="219bf-104">SYNTAX</span></span>

### <span data-ttu-id="219bf-105">Domyślne</span><span class="sxs-lookup"><span data-stu-id="219bf-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219bf-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="219bf-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="219bf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="219bf-107">DESCRIPTION</span></span>
<span data-ttu-id="219bf-108">Polecenie cmdlet **Remove-AzureKeyVaultCertificateOperation** usuwa operację certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="219bf-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="219bf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="219bf-109">EXAMPLES</span></span>

### <span data-ttu-id="219bf-110">Przykład 1: usuwanie operacji na certyfikacie</span><span class="sxs-lookup"><span data-stu-id="219bf-110">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="219bf-111">To polecenie usuwa operację certyfikatu o nazwie TestCert01 z magazynu kluczy ContosoKV01 bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="219bf-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="219bf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="219bf-112">PARAMETERS</span></span>

### <span data-ttu-id="219bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219bf-113">-DefaultProfile</span></span>
<span data-ttu-id="219bf-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="219bf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="219bf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="219bf-115">-Force</span></span>
<span data-ttu-id="219bf-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="219bf-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="219bf-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="219bf-117">-InputObject</span></span>
<span data-ttu-id="219bf-118">Obiekt Operation</span><span class="sxs-lookup"><span data-stu-id="219bf-118">Operation object</span></span>

```yaml
Type: PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="219bf-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="219bf-119">-Name</span></span>
<span data-ttu-id="219bf-120">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="219bf-120">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="219bf-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="219bf-121">-PassThru</span></span>
<span data-ttu-id="219bf-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="219bf-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="219bf-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="219bf-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="219bf-124">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="219bf-124">-VaultName</span></span>
<span data-ttu-id="219bf-125">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="219bf-125">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="219bf-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="219bf-126">-Confirm</span></span>
<span data-ttu-id="219bf-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219bf-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="219bf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="219bf-128">-WhatIf</span></span>
<span data-ttu-id="219bf-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219bf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="219bf-130">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219bf-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="219bf-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="219bf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="219bf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219bf-132">CommonParameters</span></span>
<span data-ttu-id="219bf-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="219bf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219bf-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="219bf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219bf-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="219bf-135">INPUTS</span></span>

### <span data-ttu-id="219bf-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="219bf-136">None</span></span>
<span data-ttu-id="219bf-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="219bf-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="219bf-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="219bf-138">OUTPUTS</span></span>

### <span data-ttu-id="219bf-139">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="219bf-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="219bf-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="219bf-140">NOTES</span></span>

## <span data-ttu-id="219bf-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="219bf-141">RELATED LINKS</span></span>

[<span data-ttu-id="219bf-142">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="219bf-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="219bf-143">Zatrzymaj — AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="219bf-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

