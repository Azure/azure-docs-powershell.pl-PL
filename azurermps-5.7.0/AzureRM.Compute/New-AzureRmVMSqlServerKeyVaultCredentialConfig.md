---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 4e252001d1459c52a35b766d34c91050df62073d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544496"
---
# <span data-ttu-id="67775-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="67775-101">New-AzureVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="67775-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67775-102">SYNOPSIS</span></span>
<span data-ttu-id="67775-103">Tworzy obiekt konfiguracji dla poświadczenia magazynu kluczy programu SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="67775-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67775-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67775-104">SYNTAX</span></span>

```
New-AzureVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67775-105">Opis</span><span class="sxs-lookup"><span data-stu-id="67775-105">DESCRIPTION</span></span>

## <span data-ttu-id="67775-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67775-106">EXAMPLES</span></span>

## <span data-ttu-id="67775-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67775-107">PARAMETERS</span></span>

### <span data-ttu-id="67775-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="67775-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67775-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="67775-109">-CredentialName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67775-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="67775-110">-Enable</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67775-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67775-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="67775-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="67775-112">-ServicePrincipalName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67775-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="67775-113">-ServicePrincipalSecret</span></span>
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67775-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67775-114">-Confirm</span></span>
<span data-ttu-id="67775-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67775-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67775-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67775-116">-WhatIf</span></span>
<span data-ttu-id="67775-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67775-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="67775-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="67775-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67775-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67775-119">CommonParameters</span></span>
<span data-ttu-id="67775-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67775-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67775-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67775-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67775-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67775-122">INPUTS</span></span>

### <span data-ttu-id="67775-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="67775-123">None</span></span>
<span data-ttu-id="67775-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="67775-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67775-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67775-125">OUTPUTS</span></span>

## <span data-ttu-id="67775-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67775-126">NOTES</span></span>

## <span data-ttu-id="67775-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67775-127">RELATED LINKS</span></span>

