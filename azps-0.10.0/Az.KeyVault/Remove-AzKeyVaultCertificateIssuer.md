---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 204ee5a7a4d0e5247ae3de239dce650deb4cff0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891269"
---
# <span data-ttu-id="512cd-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="512cd-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="512cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="512cd-102">SYNOPSIS</span></span>
<span data-ttu-id="512cd-103">Usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="512cd-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="512cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="512cd-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="512cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="512cd-105">DESCRIPTION</span></span>
<span data-ttu-id="512cd-106">Polecenie cmdlet **Remove-AzKeyVaultCertificateIssuer** usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="512cd-106">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="512cd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="512cd-107">EXAMPLES</span></span>

### <span data-ttu-id="512cd-108">Przykład 1: usuwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="512cd-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="512cd-109">To polecenie usuwa wystawcę certyfikatu o nazwie TestIssuer01 z magazynu kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="512cd-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="512cd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="512cd-110">PARAMETERS</span></span>

### <span data-ttu-id="512cd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="512cd-111">-DefaultProfile</span></span>
<span data-ttu-id="512cd-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="512cd-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="512cd-113">-Force</span><span class="sxs-lookup"><span data-stu-id="512cd-113">-Force</span></span>
<span data-ttu-id="512cd-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="512cd-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="512cd-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="512cd-115">-Name</span></span>
<span data-ttu-id="512cd-116">Określa nazwę wystawcy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="512cd-116">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="512cd-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="512cd-117">-PassThru</span></span>
<span data-ttu-id="512cd-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="512cd-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="512cd-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="512cd-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="512cd-120">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="512cd-120">-VaultName</span></span>
<span data-ttu-id="512cd-121">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="512cd-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="512cd-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="512cd-122">-Confirm</span></span>
<span data-ttu-id="512cd-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="512cd-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="512cd-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="512cd-124">-WhatIf</span></span>
<span data-ttu-id="512cd-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="512cd-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="512cd-126">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="512cd-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="512cd-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="512cd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="512cd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="512cd-128">CommonParameters</span></span>
<span data-ttu-id="512cd-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="512cd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="512cd-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="512cd-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="512cd-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="512cd-131">INPUTS</span></span>

### <span data-ttu-id="512cd-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="512cd-132">None</span></span>
<span data-ttu-id="512cd-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="512cd-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="512cd-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="512cd-134">OUTPUTS</span></span>

### <span data-ttu-id="512cd-135">Microsoft. Azure. Commands. platforming. models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="512cd-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="512cd-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="512cd-136">NOTES</span></span>

## <span data-ttu-id="512cd-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="512cd-137">RELATED LINKS</span></span>

[<span data-ttu-id="512cd-138">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="512cd-138">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="512cd-139">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="512cd-139">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


