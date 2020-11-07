---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
ms.openlocfilehash: ee627065d1d6be8037d1a9b054ec6452b9becb41
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898978"
---
# <span data-ttu-id="d0a32-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="d0a32-101">New-AzureRmVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="d0a32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0a32-102">SYNOPSIS</span></span>
<span data-ttu-id="d0a32-103">Tworzy obiekt konfiguracji dla poświadczenia magazynu kluczy programu SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d0a32-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0a32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0a32-104">SYNTAX</span></span>

```
New-AzureRmVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable]
 [-CredentialName <String>] [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>]
 [-ServicePrincipalSecret <SecureString>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0a32-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0a32-105">DESCRIPTION</span></span>

## <span data-ttu-id="d0a32-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0a32-106">EXAMPLES</span></span>

## <span data-ttu-id="d0a32-107">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0a32-107">PARAMETERS</span></span>

### <span data-ttu-id="d0a32-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="d0a32-108">-AzureKeyVaultUrl</span></span>
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

### <span data-ttu-id="d0a32-109">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="d0a32-109">-CredentialName</span></span>
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

### <span data-ttu-id="d0a32-110">-Enable</span><span class="sxs-lookup"><span data-stu-id="d0a32-110">-Enable</span></span>
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

### <span data-ttu-id="d0a32-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0a32-111">-ResourceGroupName</span></span>
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

### <span data-ttu-id="d0a32-112">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d0a32-112">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="d0a32-113">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="d0a32-113">-ServicePrincipalSecret</span></span>
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

### <span data-ttu-id="d0a32-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0a32-114">-Confirm</span></span>
<span data-ttu-id="d0a32-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0a32-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0a32-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0a32-116">-WhatIf</span></span>
<span data-ttu-id="d0a32-117">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0a32-117">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d0a32-118">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d0a32-118">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0a32-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0a32-119">CommonParameters</span></span>
<span data-ttu-id="d0a32-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0a32-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0a32-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0a32-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0a32-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0a32-122">INPUTS</span></span>

### <span data-ttu-id="d0a32-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d0a32-123">None</span></span>
<span data-ttu-id="d0a32-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d0a32-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0a32-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0a32-125">OUTPUTS</span></span>

### <span data-ttu-id="d0a32-126">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="d0a32-126">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="d0a32-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0a32-127">NOTES</span></span>

## <span data-ttu-id="d0a32-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0a32-128">RELATED LINKS</span></span>

