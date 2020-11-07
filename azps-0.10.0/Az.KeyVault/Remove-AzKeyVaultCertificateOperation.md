---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateOperation.md
ms.openlocfilehash: 37cc2025b97e16a2af313a2f4dd2cf7dfe815b7b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891262"
---
# <span data-ttu-id="1485d-101">Remove-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1485d-101">Remove-AzKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="1485d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1485d-102">SYNOPSIS</span></span>
<span data-ttu-id="1485d-103">Usuwa operację certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1485d-103">Deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="1485d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1485d-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1485d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1485d-105">DESCRIPTION</span></span>
<span data-ttu-id="1485d-106">Polecenie cmdlet **Remove-AzKeyVaultCertificateOperation** usuwa operację certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1485d-106">The **Remove-AzKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="1485d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1485d-107">EXAMPLES</span></span>

### <span data-ttu-id="1485d-108">Przykład 1: usuwanie operacji na certyfikacie</span><span class="sxs-lookup"><span data-stu-id="1485d-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="1485d-109">To polecenie usuwa operację certyfikatu o nazwie TestCert01 z magazynu kluczy ContosoKV01 bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1485d-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="1485d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1485d-110">PARAMETERS</span></span>

### <span data-ttu-id="1485d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1485d-111">-DefaultProfile</span></span>
<span data-ttu-id="1485d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1485d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1485d-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1485d-113">-Force</span></span>
<span data-ttu-id="1485d-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1485d-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1485d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1485d-115">-Name</span></span>
<span data-ttu-id="1485d-116">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="1485d-116">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1485d-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1485d-117">-PassThru</span></span>
<span data-ttu-id="1485d-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="1485d-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="1485d-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1485d-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1485d-120">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="1485d-120">-VaultName</span></span>
<span data-ttu-id="1485d-121">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="1485d-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="1485d-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1485d-122">-Confirm</span></span>
<span data-ttu-id="1485d-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1485d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1485d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1485d-124">-WhatIf</span></span>
<span data-ttu-id="1485d-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1485d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1485d-126">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1485d-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1485d-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1485d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1485d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1485d-128">CommonParameters</span></span>
<span data-ttu-id="1485d-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1485d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1485d-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1485d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1485d-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1485d-131">INPUTS</span></span>

### <span data-ttu-id="1485d-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1485d-132">None</span></span>
<span data-ttu-id="1485d-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1485d-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1485d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1485d-134">OUTPUTS</span></span>

### <span data-ttu-id="1485d-135">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1485d-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="1485d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1485d-136">NOTES</span></span>

## <span data-ttu-id="1485d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1485d-137">RELATED LINKS</span></span>

[<span data-ttu-id="1485d-138">Get-AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1485d-138">Get-AzKeyVaultCertificateOperation</span></span>](./Get-AzKeyVaultCertificateOperation.md)

[<span data-ttu-id="1485d-139">Zatrzymaj — AzKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="1485d-139">Stop-AzKeyVaultCertificateOperation</span></span>](./Stop-AzKeyVaultCertificateOperation.md)

