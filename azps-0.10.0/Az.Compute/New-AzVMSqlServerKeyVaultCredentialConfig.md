---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: d9f732a40b61687d7970fdf24f9f9f0f841b2cc7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893614"
---
# <span data-ttu-id="e1cc4-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="e1cc4-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="e1cc4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="e1cc4-103">Tworzy obiekt konfiguracji dla poświadczenia magazynu kluczy programu SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e1cc4-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="e1cc4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1cc4-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1cc4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e1cc4-105">DESCRIPTION</span></span>

## <span data-ttu-id="e1cc4-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1cc4-106">EXAMPLES</span></span>

## <span data-ttu-id="e1cc4-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1cc4-107">PARAMETERS</span></span>

### <span data-ttu-id="e1cc4-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="e1cc4-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="e1cc4-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="e1cc4-109">-CredentialName</span></span>
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

### <span data-ttu-id="e1cc4-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="e1cc4-110">-Enable</span></span>
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

### <span data-ttu-id="e1cc4-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1cc4-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="e1cc4-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e1cc4-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="e1cc4-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="e1cc4-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="e1cc4-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1cc4-114">-Confirm</span></span>
<span data-ttu-id="e1cc4-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1cc4-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1cc4-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1cc4-116">-WhatIf</span></span>
<span data-ttu-id="e1cc4-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1cc4-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e1cc4-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1cc4-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1cc4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1cc4-119">CommonParameters</span></span>
<span data-ttu-id="e1cc4-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1cc4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1cc4-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1cc4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1cc4-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1cc4-122">INPUTS</span></span>

### <span data-ttu-id="e1cc4-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e1cc4-123">None</span></span>
<span data-ttu-id="e1cc4-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e1cc4-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1cc4-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1cc4-125">OUTPUTS</span></span>

### <span data-ttu-id="e1cc4-126">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="e1cc4-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="e1cc4-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1cc4-127">NOTES</span></span>

## <span data-ttu-id="e1cc4-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1cc4-128">RELATED LINKS</span></span>

