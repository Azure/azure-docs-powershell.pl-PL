---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: dc1ea08b0770c7438574d4ef2cc6a97cb99f2909
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717465"
---
# <span data-ttu-id="e4f82-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="e4f82-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="e4f82-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4f82-102">SYNOPSIS</span></span>
<span data-ttu-id="e4f82-103">Tworzy obiekt konfiguracji dla poświadczenia magazynu kluczy programu SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e4f82-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4f82-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4f82-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4f82-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4f82-105">DESCRIPTION</span></span>

## <span data-ttu-id="e4f82-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4f82-106">EXAMPLES</span></span>

## <span data-ttu-id="e4f82-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4f82-107">PARAMETERS</span></span>

### <span data-ttu-id="e4f82-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="e4f82-108">-AzureKeyVaultUrl</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f82-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="e4f82-109">-CredentialName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f82-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="e4f82-110">-Enable</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f82-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4f82-111">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f82-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e4f82-112">-ServicePrincipalName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f82-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="e4f82-113">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4f82-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4f82-114">-Confirm</span></span>
<span data-ttu-id="e4f82-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4f82-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4f82-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4f82-116">-WhatIf</span></span>
<span data-ttu-id="e4f82-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4f82-117">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4f82-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4f82-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4f82-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4f82-119">CommonParameters</span></span>
<span data-ttu-id="e4f82-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4f82-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4f82-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4f82-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4f82-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4f82-122">INPUTS</span></span>

### <span data-ttu-id="e4f82-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e4f82-123">System.String</span></span>

### <span data-ttu-id="e4f82-124">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e4f82-124">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e4f82-125">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="e4f82-125">System.Security.SecureString</span></span>

## <span data-ttu-id="e4f82-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4f82-126">OUTPUTS</span></span>

### <span data-ttu-id="e4f82-127">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="e4f82-127">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="e4f82-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4f82-128">NOTES</span></span>

## <span data-ttu-id="e4f82-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4f82-129">RELATED LINKS</span></span>
