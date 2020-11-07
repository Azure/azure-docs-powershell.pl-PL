---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b41f7cb1c5e3ebec58e3866c94d8e2c62bdf670b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542320"
---
# <span data-ttu-id="b5636-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="b5636-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="b5636-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5636-102">SYNOPSIS</span></span>
<span data-ttu-id="b5636-103">Rejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="b5636-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5636-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5636-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5636-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5636-105">DESCRIPTION</span></span>
<span data-ttu-id="b5636-106">Polecenie cmdlet **register-AzureRmProviderFeature** rejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="b5636-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="b5636-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5636-107">EXAMPLES</span></span>

### <span data-ttu-id="b5636-108">Przykład 1. rejestrowanie funkcji</span><span class="sxs-lookup"><span data-stu-id="b5636-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="b5636-109">Spowoduje to dodanie funkcji AllowApplicationSecurityGroups dla usługi Microsoft. Network do konta.</span><span class="sxs-lookup"><span data-stu-id="b5636-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="b5636-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5636-110">PARAMETERS</span></span>

### <span data-ttu-id="b5636-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5636-111">-DefaultProfile</span></span>
<span data-ttu-id="b5636-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b5636-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5636-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="b5636-113">-FeatureName</span></span>
<span data-ttu-id="b5636-114">Określa nazwę funkcji, którą to polecenie cmdlet rejestruje.</span><span class="sxs-lookup"><span data-stu-id="b5636-114">Specifies the name of the feature that this cmdlet registers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5636-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="b5636-115">-ProviderNamespace</span></span>
<span data-ttu-id="b5636-116">Określa obszar nazw, dla którego to polecenie cmdlet rejestruje funkcję dostawcy.</span><span class="sxs-lookup"><span data-stu-id="b5636-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5636-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5636-117">-Confirm</span></span>
<span data-ttu-id="b5636-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5636-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5636-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5636-119">-WhatIf</span></span>
<span data-ttu-id="b5636-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5636-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5636-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5636-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5636-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5636-122">CommonParameters</span></span>
<span data-ttu-id="b5636-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5636-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5636-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5636-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5636-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5636-125">INPUTS</span></span>

### <span data-ttu-id="b5636-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b5636-126">None</span></span>
<span data-ttu-id="b5636-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b5636-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5636-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5636-128">OUTPUTS</span></span>

### <span data-ttu-id="b5636-129">System. Collections. Generic. list "1 [Microsoft. Azure. Commands.</span><span class="sxs-lookup"><span data-stu-id="b5636-129">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="b5636-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5636-130">NOTES</span></span>

## <span data-ttu-id="b5636-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5636-131">RELATED LINKS</span></span>

[<span data-ttu-id="b5636-132">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="b5636-132">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)

