---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 35cb8ad956419a2fcbfe427ce23e518986da63ab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490346"
---
# <span data-ttu-id="dd466-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="dd466-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="dd466-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd466-102">SYNOPSIS</span></span>
<span data-ttu-id="dd466-103">Rejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="dd466-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="dd466-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd466-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd466-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd466-105">DESCRIPTION</span></span>
<span data-ttu-id="dd466-106">Polecenie cmdlet **register-AzProviderFeature** rejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="dd466-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="dd466-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd466-107">EXAMPLES</span></span>

### <span data-ttu-id="dd466-108">Przykład 1. rejestrowanie funkcji</span><span class="sxs-lookup"><span data-stu-id="dd466-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="dd466-109">Spowoduje to dodanie funkcji AllowApplicationSecurityGroups dla usługi Microsoft. Network do konta.</span><span class="sxs-lookup"><span data-stu-id="dd466-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="dd466-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd466-110">PARAMETERS</span></span>

### <span data-ttu-id="dd466-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd466-111">-DefaultProfile</span></span>
<span data-ttu-id="dd466-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dd466-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dd466-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="dd466-113">-FeatureName</span></span>
<span data-ttu-id="dd466-114">Określa nazwę funkcji, którą to polecenie cmdlet rejestruje.</span><span class="sxs-lookup"><span data-stu-id="dd466-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="dd466-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="dd466-115">-ProviderNamespace</span></span>
<span data-ttu-id="dd466-116">Określa obszar nazw, dla którego to polecenie cmdlet rejestruje funkcję dostawcy.</span><span class="sxs-lookup"><span data-stu-id="dd466-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="dd466-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd466-117">-Confirm</span></span>
<span data-ttu-id="dd466-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd466-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd466-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd466-119">-WhatIf</span></span>
<span data-ttu-id="dd466-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd466-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd466-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dd466-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd466-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd466-122">CommonParameters</span></span>
<span data-ttu-id="dd466-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd466-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd466-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dd466-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd466-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd466-125">INPUTS</span></span>

### <span data-ttu-id="dd466-126">System. String</span><span class="sxs-lookup"><span data-stu-id="dd466-126">System.String</span></span>

## <span data-ttu-id="dd466-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd466-127">OUTPUTS</span></span>

### <span data-ttu-id="dd466-128">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="dd466-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="dd466-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd466-129">NOTES</span></span>

## <span data-ttu-id="dd466-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd466-130">RELATED LINKS</span></span>

[<span data-ttu-id="dd466-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="dd466-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


