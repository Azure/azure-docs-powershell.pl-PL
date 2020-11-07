---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 4c732cdfc175c47e9bd8125234cb1d33f1b19097
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93897378"
---
# <span data-ttu-id="2e8b3-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2e8b3-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2e8b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e8b3-102">SYNOPSIS</span></span>
<span data-ttu-id="2e8b3-103">Usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e8b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e8b3-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e8b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e8b3-105">DESCRIPTION</span></span>
<span data-ttu-id="2e8b3-106">Polecenie cmdlet **Remove-AzureKeyVaultCertificateIssuer** usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="2e8b3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e8b3-107">EXAMPLES</span></span>

### <span data-ttu-id="2e8b3-108">Przykład 1: usuwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="2e8b3-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="2e8b3-109">To polecenie usuwa wystawcę certyfikatu o nazwie TestIssuer01 z magazynu kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="2e8b3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e8b3-110">PARAMETERS</span></span>

### <span data-ttu-id="2e8b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e8b3-111">-DefaultProfile</span></span>
<span data-ttu-id="2e8b3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2e8b3-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e8b3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2e8b3-113">-Force</span></span>
<span data-ttu-id="2e8b3-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2e8b3-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e8b3-115">-Name</span></span>
<span data-ttu-id="2e8b3-116">Określa nazwę wystawcy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e8b3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e8b3-117">-PassThru</span></span>
<span data-ttu-id="2e8b3-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2e8b3-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2e8b3-120">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="2e8b3-120">-VaultName</span></span>
<span data-ttu-id="2e8b3-121">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="2e8b3-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e8b3-122">-Confirm</span></span>
<span data-ttu-id="2e8b3-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e8b3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e8b3-124">-WhatIf</span></span>
<span data-ttu-id="2e8b3-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e8b3-126">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e8b3-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e8b3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e8b3-128">CommonParameters</span></span>
<span data-ttu-id="2e8b3-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e8b3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e8b3-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e8b3-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e8b3-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e8b3-131">INPUTS</span></span>

## <span data-ttu-id="2e8b3-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e8b3-132">OUTPUTS</span></span>

### <span data-ttu-id="2e8b3-133">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2e8b3-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="2e8b3-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e8b3-134">NOTES</span></span>

## <span data-ttu-id="2e8b3-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e8b3-135">RELATED LINKS</span></span>

[<span data-ttu-id="2e8b3-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2e8b3-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="2e8b3-137">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="2e8b3-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


