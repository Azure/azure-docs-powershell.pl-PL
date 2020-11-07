---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/register-azurermproviderfeature
schema: 2.0.0
ms.openlocfilehash: 2371ea9a50af1d23144560acbf4fd88679f0e50d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899038"
---
# <span data-ttu-id="c60fe-101">Register-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c60fe-101">Register-AzureRmProviderFeature</span></span>

## <span data-ttu-id="c60fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c60fe-102">SYNOPSIS</span></span>
<span data-ttu-id="c60fe-103">Rejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="c60fe-103">Registers an Azure provider feature in your account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c60fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c60fe-104">SYNTAX</span></span>

```
Register-AzureRmProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c60fe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c60fe-105">DESCRIPTION</span></span>
<span data-ttu-id="c60fe-106">Polecenie cmdlet **register-AzureRmProviderFeature** rejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="c60fe-106">The **Register-AzureRmProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="c60fe-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c60fe-107">EXAMPLES</span></span>

### <span data-ttu-id="c60fe-108">Przykład 1. rejestrowanie funkcji</span><span class="sxs-lookup"><span data-stu-id="c60fe-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzureRmProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="c60fe-109">Spowoduje to dodanie funkcji AllowApplicationSecurityGroups dla usługi Microsoft. Network do konta.</span><span class="sxs-lookup"><span data-stu-id="c60fe-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="c60fe-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c60fe-110">PARAMETERS</span></span>

### <span data-ttu-id="c60fe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c60fe-111">-DefaultProfile</span></span>
<span data-ttu-id="c60fe-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c60fe-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c60fe-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="c60fe-113">-FeatureName</span></span>
<span data-ttu-id="c60fe-114">Określa nazwę funkcji, którą to polecenie cmdlet rejestruje.</span><span class="sxs-lookup"><span data-stu-id="c60fe-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="c60fe-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="c60fe-115">-ProviderNamespace</span></span>
<span data-ttu-id="c60fe-116">Określa obszar nazw, dla którego to polecenie cmdlet rejestruje funkcję dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c60fe-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="c60fe-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c60fe-117">-Confirm</span></span>
<span data-ttu-id="c60fe-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c60fe-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c60fe-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c60fe-119">-WhatIf</span></span>
<span data-ttu-id="c60fe-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c60fe-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c60fe-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c60fe-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c60fe-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c60fe-122">CommonParameters</span></span>
<span data-ttu-id="c60fe-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c60fe-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c60fe-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c60fe-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c60fe-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c60fe-125">INPUTS</span></span>

## <span data-ttu-id="c60fe-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c60fe-126">OUTPUTS</span></span>

## <span data-ttu-id="c60fe-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c60fe-127">NOTES</span></span>

## <span data-ttu-id="c60fe-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c60fe-128">RELATED LINKS</span></span>

[<span data-ttu-id="c60fe-129">Get-AzureRmProviderFeature</span><span class="sxs-lookup"><span data-stu-id="c60fe-129">Get-AzureRmProviderFeature</span></span>](./Get-AzureRmProviderFeature.md)


