---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 3ef23bcbddc1f8a5c5c235c72dac32f535a71a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551872"
---
# <span data-ttu-id="b9670-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b9670-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b9670-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9670-102">SYNOPSIS</span></span>
<span data-ttu-id="b9670-103">Usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b9670-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9670-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9670-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9670-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9670-105">DESCRIPTION</span></span>
<span data-ttu-id="b9670-106">Polecenie cmdlet **Remove-AzureKeyVaultCertificateIssuer** usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b9670-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="b9670-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9670-107">EXAMPLES</span></span>

### <span data-ttu-id="b9670-108">Przykład 1: usuwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b9670-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="b9670-109">To polecenie usuwa wystawcę certyfikatu o nazwie TestIssuer01 z magazynu kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="b9670-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="b9670-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9670-110">PARAMETERS</span></span>

### <span data-ttu-id="b9670-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b9670-111">-Force</span></span>
<span data-ttu-id="b9670-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b9670-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9670-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b9670-113">-Name</span></span>
<span data-ttu-id="b9670-114">Określa nazwę wystawcy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="b9670-114">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9670-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9670-115">-PassThru</span></span>
<span data-ttu-id="b9670-116">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="b9670-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b9670-117">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="b9670-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b9670-118">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="b9670-118">-VaultName</span></span>
<span data-ttu-id="b9670-119">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="b9670-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="b9670-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9670-120">-Confirm</span></span>
<span data-ttu-id="b9670-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9670-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9670-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9670-122">-WhatIf</span></span>
<span data-ttu-id="b9670-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9670-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9670-124">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9670-124">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9670-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9670-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9670-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9670-126">-DefaultProfile</span></span>
<span data-ttu-id="b9670-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9670-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9670-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9670-128">CommonParameters</span></span>
<span data-ttu-id="b9670-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9670-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9670-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9670-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9670-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9670-131">INPUTS</span></span>

## <span data-ttu-id="b9670-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9670-132">OUTPUTS</span></span>

### <span data-ttu-id="b9670-133">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b9670-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b9670-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9670-134">NOTES</span></span>

## <span data-ttu-id="b9670-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9670-135">RELATED LINKS</span></span>

[<span data-ttu-id="b9670-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b9670-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="b9670-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b9670-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


