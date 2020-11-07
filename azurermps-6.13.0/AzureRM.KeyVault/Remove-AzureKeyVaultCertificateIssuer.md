---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: dc49237d4722384d04228d3b8e9736411ed41bde
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717188"
---
# <span data-ttu-id="41c78-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="41c78-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="41c78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41c78-102">SYNOPSIS</span></span>
<span data-ttu-id="41c78-103">Usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="41c78-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41c78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41c78-104">SYNTAX</span></span>

### <span data-ttu-id="41c78-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="41c78-105">Default (Default)</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41c78-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="41c78-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41c78-107">Opis</span><span class="sxs-lookup"><span data-stu-id="41c78-107">DESCRIPTION</span></span>
<span data-ttu-id="41c78-108">Polecenie cmdlet **Remove-AzureKeyVaultCertificateIssuer** usuwa wystawcę certyfikatu z magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="41c78-108">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="41c78-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41c78-109">EXAMPLES</span></span>

### <span data-ttu-id="41c78-110">Przykład 1: usuwanie wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="41c78-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="41c78-111">To polecenie usuwa wystawcę certyfikatu o nazwie TestIssuer01 z magazynu kluczy ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="41c78-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="41c78-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41c78-112">PARAMETERS</span></span>

### <span data-ttu-id="41c78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41c78-113">-DefaultProfile</span></span>
<span data-ttu-id="41c78-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="41c78-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41c78-115">-Force</span><span class="sxs-lookup"><span data-stu-id="41c78-115">-Force</span></span>
<span data-ttu-id="41c78-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="41c78-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41c78-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="41c78-117">-InputObject</span></span>
<span data-ttu-id="41c78-118">Obiekt wystawcy certyfikatu</span><span class="sxs-lookup"><span data-stu-id="41c78-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41c78-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41c78-119">-Name</span></span>
<span data-ttu-id="41c78-120">Określa nazwę wystawcy do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="41c78-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c78-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41c78-121">-PassThru</span></span>
<span data-ttu-id="41c78-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="41c78-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="41c78-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="41c78-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="41c78-124">-Magazynname</span><span class="sxs-lookup"><span data-stu-id="41c78-124">-VaultName</span></span>
<span data-ttu-id="41c78-125">Określa nazwę magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="41c78-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41c78-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41c78-126">-Confirm</span></span>
<span data-ttu-id="41c78-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41c78-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41c78-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41c78-128">-WhatIf</span></span>
<span data-ttu-id="41c78-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41c78-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c78-130">Polecenie cmdlet nie jest uruchamiane. Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41c78-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41c78-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41c78-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41c78-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41c78-132">CommonParameters</span></span>
<span data-ttu-id="41c78-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41c78-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41c78-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41c78-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41c78-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41c78-135">INPUTS</span></span>

### <span data-ttu-id="41c78-136">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="41c78-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="41c78-137">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="41c78-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="41c78-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41c78-138">OUTPUTS</span></span>

### <span data-ttu-id="41c78-139">Microsoft. Azure. Commands. platforming. models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="41c78-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="41c78-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41c78-140">NOTES</span></span>

## <span data-ttu-id="41c78-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41c78-141">RELATED LINKS</span></span>

[<span data-ttu-id="41c78-142">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="41c78-142">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="41c78-143">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="41c78-143">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


