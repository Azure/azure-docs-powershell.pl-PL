---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
ms.openlocfilehash: 7d5a575bfb5e26511f2051e8e45654af1e8c9f2e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897377"
---
# <span data-ttu-id="491c1-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="491c1-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="491c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="491c1-102">SYNOPSIS</span></span>
<span data-ttu-id="491c1-103">Usuwa operację certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="491c1-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="491c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="491c1-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="491c1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="491c1-105">DESCRIPTION</span></span>
<span data-ttu-id="491c1-106">Polecenie cmdlet **Remove-AzureKeyVaultCertificateOperation** usuwa operację certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="491c1-106">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="491c1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="491c1-107">EXAMPLES</span></span>

### <span data-ttu-id="491c1-108">Przykład 1: usuwanie operacji na certyfikacie</span><span class="sxs-lookup"><span data-stu-id="491c1-108">Example 1: Remove a certificate operation</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force
```

<span data-ttu-id="491c1-109">To polecenie usuwa operację certyfikatu o nazwie TestCert01 z magazynu kluczy ContosoKV01 bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="491c1-109">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="491c1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="491c1-110">PARAMETERS</span></span>

### <span data-ttu-id="491c1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="491c1-111">-DefaultProfile</span></span>
<span data-ttu-id="491c1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="491c1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="491c1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="491c1-113">-Force</span></span>
<span data-ttu-id="491c1-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="491c1-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="491c1-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="491c1-115">-Name</span></span>
<span data-ttu-id="491c1-116">Określa nazwę certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="491c1-116">Specifies the name of a certificate.</span></span>

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

### <span data-ttu-id="491c1-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="491c1-117">-PassThru</span></span>
<span data-ttu-id="491c1-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="491c1-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="491c1-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="491c1-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="491c1-120">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="491c1-120">-VaultName</span></span>
<span data-ttu-id="491c1-121">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="491c1-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="491c1-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="491c1-122">-Confirm</span></span>
<span data-ttu-id="491c1-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="491c1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="491c1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="491c1-124">-WhatIf</span></span>
<span data-ttu-id="491c1-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="491c1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="491c1-126">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="491c1-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="491c1-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="491c1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="491c1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="491c1-128">CommonParameters</span></span>
<span data-ttu-id="491c1-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="491c1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="491c1-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="491c1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="491c1-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="491c1-131">INPUTS</span></span>

## <span data-ttu-id="491c1-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="491c1-132">OUTPUTS</span></span>

### <span data-ttu-id="491c1-133">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="491c1-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOperation</span></span>

## <span data-ttu-id="491c1-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="491c1-134">NOTES</span></span>

## <span data-ttu-id="491c1-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="491c1-135">RELATED LINKS</span></span>

[<span data-ttu-id="491c1-136">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="491c1-136">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="491c1-137">Zatrzymaj — AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="491c1-137">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

