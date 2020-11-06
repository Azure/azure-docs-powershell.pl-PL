---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/remove-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Remove-AzureRmAks.md
ms.openlocfilehash: 1843322f702f8c43f97f1cf64c9d9f5b92d419bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549811"
---
# <span data-ttu-id="e8af6-101">Remove-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="e8af6-101">Remove-AzureRmAks</span></span>

## <span data-ttu-id="e8af6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8af6-102">SYNOPSIS</span></span>
<span data-ttu-id="e8af6-103">Usuń zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e8af6-103">Delete a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8af6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8af6-104">SYNTAX</span></span>

### <span data-ttu-id="e8af6-105">GroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e8af6-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8af6-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8af6-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8af6-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8af6-107">IdParameterSet</span></span>
```
Remove-AzureRmAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8af6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e8af6-108">DESCRIPTION</span></span>
<span data-ttu-id="e8af6-109">Usuń zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e8af6-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e8af6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8af6-110">EXAMPLES</span></span>

### <span data-ttu-id="e8af6-111">Usuwanie istniejącego klastra zarządzanego Kubernetes</span><span class="sxs-lookup"><span data-stu-id="e8af6-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="e8af6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8af6-112">PARAMETERS</span></span>

### <span data-ttu-id="e8af6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8af6-113">-AsJob</span></span>
<span data-ttu-id="e8af6-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e8af6-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8af6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8af6-115">-DefaultProfile</span></span>
<span data-ttu-id="e8af6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8af6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8af6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e8af6-117">-Force</span></span>
<span data-ttu-id="e8af6-118">Usuwanie zarządzanego klastra Kubernetes bez monitowania</span><span class="sxs-lookup"><span data-stu-id="e8af6-118">Remove managed Kubernetes cluster without prompt</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8af6-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e8af6-119">-Id</span></span>
<span data-ttu-id="e8af6-120">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="e8af6-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8af6-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e8af6-121">-InputObject</span></span>
<span data-ttu-id="e8af6-122">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="e8af6-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8af6-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e8af6-123">-Name</span></span>
<span data-ttu-id="e8af6-124">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="e8af6-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8af6-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8af6-125">-PassThru</span></span>
<span data-ttu-id="e8af6-126">Zwraca wartość PRAWDA, Jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="e8af6-126">Returns true if deletion is successful</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8af6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8af6-127">-ResourceGroupName</span></span>
<span data-ttu-id="e8af6-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e8af6-128">Resource group name</span></span>

```yaml
Type: String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8af6-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8af6-129">-Confirm</span></span>
<span data-ttu-id="e8af6-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8af6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8af6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8af6-131">-WhatIf</span></span>
<span data-ttu-id="e8af6-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8af6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8af6-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8af6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8af6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8af6-134">CommonParameters</span></span>
<span data-ttu-id="e8af6-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8af6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8af6-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8af6-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8af6-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8af6-137">INPUTS</span></span>

### <span data-ttu-id="e8af6-138">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e8af6-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="e8af6-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e8af6-139">System.String</span></span>

## <span data-ttu-id="e8af6-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8af6-140">OUTPUTS</span></span>

### <span data-ttu-id="e8af6-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8af6-141">System.Boolean</span></span>

## <span data-ttu-id="e8af6-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8af6-142">NOTES</span></span>

## <span data-ttu-id="e8af6-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8af6-143">RELATED LINKS</span></span>
