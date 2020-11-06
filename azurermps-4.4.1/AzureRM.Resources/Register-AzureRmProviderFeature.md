---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Register-AzureRmProviderFeature.md
ms.openlocfilehash: b519108918f2c26d86807302314a4defed1a0050
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549887"
---
# <span data-ttu-id="d56be-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d56be-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="d56be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d56be-102">SYNOPSIS</span></span>
<span data-ttu-id="d56be-103">Rejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="d56be-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d56be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d56be-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d56be-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d56be-105">DESCRIPTION</span></span>
<span data-ttu-id="d56be-106">Polecenie cmdlet **register-AzureRmProviderFeature** rejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="d56be-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="d56be-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d56be-107">EXAMPLES</span></span>

## <span data-ttu-id="d56be-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d56be-108">PARAMETERS</span></span>

### <span data-ttu-id="d56be-109">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="d56be-109">-FeatureName</span></span>
<span data-ttu-id="d56be-110">Określa nazwę funkcji, którą to polecenie cmdlet rejestruje.</span><span class="sxs-lookup"><span data-stu-id="d56be-110">Specifies the name of the feature that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d56be-111">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="d56be-111">-ProviderNamespace</span></span>
<span data-ttu-id="d56be-112">Określa obszar nazw, dla którego to polecenie cmdlet rejestruje funkcję dostawcy.</span><span class="sxs-lookup"><span data-stu-id="d56be-112">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d56be-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d56be-113">-Confirm</span></span>
<span data-ttu-id="d56be-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d56be-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d56be-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d56be-115">-WhatIf</span></span>
<span data-ttu-id="d56be-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d56be-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d56be-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d56be-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d56be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d56be-118">-DefaultProfile</span></span>
<span data-ttu-id="d56be-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d56be-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d56be-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d56be-120">CommonParameters</span></span>
<span data-ttu-id="d56be-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d56be-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d56be-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d56be-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d56be-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d56be-123">INPUTS</span></span>

## <span data-ttu-id="d56be-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d56be-124">OUTPUTS</span></span>

### <span data-ttu-id="d56be-125">System. Collections. Generic. list "1 [Microsoft. Azure. Commands.</span><span class="sxs-lookup"><span data-stu-id="d56be-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature]</span></span>

## <span data-ttu-id="d56be-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d56be-126">NOTES</span></span>

## <span data-ttu-id="d56be-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d56be-127">RELATED LINKS</span></span>

[<span data-ttu-id="d56be-128">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="d56be-128">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


