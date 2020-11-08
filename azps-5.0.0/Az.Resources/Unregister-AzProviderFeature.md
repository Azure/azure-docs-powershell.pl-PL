---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232671"
---
# <span data-ttu-id="e9e6c-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="e9e6c-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="e9e6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9e6c-102">SYNOPSIS</span></span>
<span data-ttu-id="e9e6c-103">Wyrejestrowuje funkcję dostawcy platformy Azure na koncie.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="e9e6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9e6c-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9e6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e9e6c-105">DESCRIPTION</span></span>
<span data-ttu-id="e9e6c-106">Polecenie cmdlet **Unregister-AzProviderFeature** umożliwia Wyrejestrowanie funkcji dostawcy platformy Azure na koncie.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="e9e6c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9e6c-107">EXAMPLES</span></span>

### <span data-ttu-id="e9e6c-108">Przykład 1. Wyrejestrowanie funkcji</span><span class="sxs-lookup"><span data-stu-id="e9e6c-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="e9e6c-109">Spowoduje to Wyrejestrowanie funkcji AllowApplicationSecurityGroups dla usługi Microsoft. Network ze swojego konta.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="e9e6c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9e6c-110">PARAMETERS</span></span>

### <span data-ttu-id="e9e6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9e6c-111">-DefaultProfile</span></span>
<span data-ttu-id="e9e6c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e6c-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="e9e6c-113">-FeatureName</span></span>
<span data-ttu-id="e9e6c-114">Nazwa funkcji.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-114">The feature name.</span></span>

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

### <span data-ttu-id="e9e6c-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e9e6c-115">-ProviderNamespace</span></span>
<span data-ttu-id="e9e6c-116">Obszar nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-116">The resource provider namespace.</span></span>

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

### <span data-ttu-id="e9e6c-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9e6c-117">-Confirm</span></span>
<span data-ttu-id="e9e6c-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e6c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9e6c-119">-WhatIf</span></span>
<span data-ttu-id="e9e6c-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9e6c-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9e6c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9e6c-122">CommonParameters</span></span>
<span data-ttu-id="e9e6c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9e6c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9e6c-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9e6c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9e6c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9e6c-125">INPUTS</span></span>

### <span data-ttu-id="e9e6c-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e9e6c-126">System.String</span></span>

## <span data-ttu-id="e9e6c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9e6c-127">OUTPUTS</span></span>

### <span data-ttu-id="e9e6c-128">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="e9e6c-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="e9e6c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9e6c-129">NOTES</span></span>

## <span data-ttu-id="e9e6c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9e6c-130">RELATED LINKS</span></span>