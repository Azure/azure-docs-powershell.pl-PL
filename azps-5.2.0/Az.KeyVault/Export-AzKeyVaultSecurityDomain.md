---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/export-azkeyvaultsecuritydomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Export-AzKeyVaultSecurityDomain.md
ms.openlocfilehash: 94f27b497450201715b423babbd55811f2382dd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372785"
---
# <span data-ttu-id="72cb5-101">Export-AzKeyVaultSecurityDomain</span><span class="sxs-lookup"><span data-stu-id="72cb5-101">Export-AzKeyVaultSecurityDomain</span></span>

## <span data-ttu-id="72cb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="72cb5-103">Eksportuje dane domeny zabezpieczeń zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="72cb5-103">Exports the security domain data of a managed HSM.</span></span>

## <span data-ttu-id="72cb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72cb5-104">SYNTAX</span></span>

### <span data-ttu-id="72cb5-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72cb5-105">ByName (Default)</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72cb5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="72cb5-106">ByInputObject</span></span>
```
Export-AzKeyVaultSecurityDomain -Certificates <String[]> -OutputPath <String> [-Force] [-PassThru]
 -Quorum <Int32> -InputObject <PSKeyVaultIdentityItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72cb5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="72cb5-107">DESCRIPTION</span></span>
<span data-ttu-id="72cb5-108">Eksportuje dane domeny zabezpieczeń zarządzanego modułu HSM w celu zaimportowania go do innego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="72cb5-108">Exports the security domain data of a managed HSM for importing on another HSM.</span></span>

## <span data-ttu-id="72cb5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72cb5-109">EXAMPLES</span></span>

### <span data-ttu-id="72cb5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72cb5-110">Example 1</span></span>
```powershell
PS C:\Users\username\> Export-AzKeyVaultSecurityDomain -Name testmhsm -Certificates {pathOfCertificates}/sd1.cer, {pathOfCertificates}/sd2.cer, {pathOfCertificates}/sd3.cer -OutputPath {pathOfOutput}/sd.ps.json -Quorum 2
```

<span data-ttu-id="72cb5-111">To polecenie umożliwia pobranie zarządzanego modułu HSM o nazwie testmhsm i zapisanie kopii zapasowej tej domeny zabezpieczeń modułu HSM w określonym pliku wyjściowym.</span><span class="sxs-lookup"><span data-stu-id="72cb5-111">This command retrieves the managed HSM named testmhsm and saves a backup of that managed HSM security domain to the specified output file.</span></span>

## <span data-ttu-id="72cb5-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72cb5-112">PARAMETERS</span></span>

### <span data-ttu-id="72cb5-113">-Certificates</span><span class="sxs-lookup"><span data-stu-id="72cb5-113">-Certificates</span></span>
<span data-ttu-id="72cb5-114">Ścieżki do certyfikatów używanych do szyfrowania danych domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="72cb5-114">Paths to the certificates that are used to encrypt the security domain data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72cb5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72cb5-115">-DefaultProfile</span></span>
<span data-ttu-id="72cb5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72cb5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72cb5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="72cb5-117">-Force</span></span>
<span data-ttu-id="72cb5-118">Określ, czy zastąpić istniejący plik.</span><span class="sxs-lookup"><span data-stu-id="72cb5-118">Specify whether to overwrite existing file.</span></span>

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

### <span data-ttu-id="72cb5-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="72cb5-119">-InputObject</span></span>
<span data-ttu-id="72cb5-120">Obiekt reprezentujący zarządzany element HSM.</span><span class="sxs-lookup"><span data-stu-id="72cb5-120">Object representing a managed HSM.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72cb5-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72cb5-121">-Name</span></span>
<span data-ttu-id="72cb5-122">Nazwa zarządzanego modułu HSM.</span><span class="sxs-lookup"><span data-stu-id="72cb5-122">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72cb5-123">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="72cb5-123">-OutputPath</span></span>
<span data-ttu-id="72cb5-124">Określ ścieżkę, do której mają być pobierane dane domeny zabezpieczeń.</span><span class="sxs-lookup"><span data-stu-id="72cb5-124">Specify the path where security domain data will be downloaded to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72cb5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72cb5-125">-PassThru</span></span>
<span data-ttu-id="72cb5-126">Po określeniu wartość logiczna zostanie zwrócona, gdy polecenie cmdlet zostanie wykonane pomyślnie.</span><span class="sxs-lookup"><span data-stu-id="72cb5-126">When specified, a boolean will be returned when cmdlet succeeds.</span></span>

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

### <span data-ttu-id="72cb5-127">-Kworum</span><span class="sxs-lookup"><span data-stu-id="72cb5-127">-Quorum</span></span>
<span data-ttu-id="72cb5-128">Minimalna liczba akcji wymaganych do odszyfrowania domeny zabezpieczeń na potrzeby odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="72cb5-128">The minimum number of shares required to decrypt the security domain for recovery.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72cb5-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72cb5-129">-Confirm</span></span>
<span data-ttu-id="72cb5-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72cb5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72cb5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72cb5-131">-WhatIf</span></span>
<span data-ttu-id="72cb5-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72cb5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72cb5-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72cb5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72cb5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72cb5-134">CommonParameters</span></span>
<span data-ttu-id="72cb5-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72cb5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72cb5-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72cb5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72cb5-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72cb5-137">INPUTS</span></span>

### <span data-ttu-id="72cb5-138">Microsoft. Azure. Commands. platforming. models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="72cb5-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="72cb5-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72cb5-139">OUTPUTS</span></span>

### <span data-ttu-id="72cb5-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="72cb5-140">System.Boolean</span></span>

## <span data-ttu-id="72cb5-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72cb5-141">NOTES</span></span>

## <span data-ttu-id="72cb5-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72cb5-142">RELATED LINKS</span></span>
