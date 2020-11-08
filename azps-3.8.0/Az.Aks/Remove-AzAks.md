---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
ms.openlocfilehash: 25a138b326a2fc086138f25a3d85f5182ba027fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050186"
---
# <span data-ttu-id="275fb-101">Remove-AzAks</span><span class="sxs-lookup"><span data-stu-id="275fb-101">Remove-AzAks</span></span>

## <span data-ttu-id="275fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="275fb-102">SYNOPSIS</span></span>
<span data-ttu-id="275fb-103">Usuń zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="275fb-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="275fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="275fb-104">SYNTAX</span></span>

### <span data-ttu-id="275fb-105">GroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="275fb-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275fb-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="275fb-106">InputObjectParameterSet</span></span>
```
Remove-AzAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="275fb-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="275fb-107">IdParameterSet</span></span>
```
Remove-AzAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="275fb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="275fb-108">DESCRIPTION</span></span>
<span data-ttu-id="275fb-109">Usuń zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="275fb-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="275fb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="275fb-110">EXAMPLES</span></span>

### <span data-ttu-id="275fb-111">Usuwanie istniejącego klastra zarządzanego Kubernetes</span><span class="sxs-lookup"><span data-stu-id="275fb-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="275fb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="275fb-112">PARAMETERS</span></span>

### <span data-ttu-id="275fb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="275fb-113">-AsJob</span></span>
<span data-ttu-id="275fb-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="275fb-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275fb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="275fb-115">-DefaultProfile</span></span>
<span data-ttu-id="275fb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="275fb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="275fb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="275fb-117">-Force</span></span>
<span data-ttu-id="275fb-118">Usuwanie zarządzanego klastra Kubernetes bez monitowania</span><span class="sxs-lookup"><span data-stu-id="275fb-118">Remove managed Kubernetes cluster without prompt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275fb-119">-ID</span><span class="sxs-lookup"><span data-stu-id="275fb-119">-Id</span></span>
<span data-ttu-id="275fb-120">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="275fb-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="275fb-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="275fb-121">-InputObject</span></span>
<span data-ttu-id="275fb-122">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="275fb-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="275fb-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="275fb-123">-Name</span></span>
<span data-ttu-id="275fb-124">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="275fb-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275fb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="275fb-125">-PassThru</span></span>
<span data-ttu-id="275fb-126">Zwraca wartość PRAWDA, Jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="275fb-126">Returns true if deletion is successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275fb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="275fb-127">-ResourceGroupName</span></span>
<span data-ttu-id="275fb-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="275fb-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275fb-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="275fb-129">-Confirm</span></span>
<span data-ttu-id="275fb-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275fb-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275fb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="275fb-131">-WhatIf</span></span>
<span data-ttu-id="275fb-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="275fb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="275fb-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="275fb-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="275fb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="275fb-134">CommonParameters</span></span>
<span data-ttu-id="275fb-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="275fb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="275fb-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="275fb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="275fb-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="275fb-137">INPUTS</span></span>

### <span data-ttu-id="275fb-138">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="275fb-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="275fb-139">System. String</span><span class="sxs-lookup"><span data-stu-id="275fb-139">System.String</span></span>

## <span data-ttu-id="275fb-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="275fb-140">OUTPUTS</span></span>

### <span data-ttu-id="275fb-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="275fb-141">System.Boolean</span></span>

## <span data-ttu-id="275fb-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="275fb-142">NOTES</span></span>

## <span data-ttu-id="275fb-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="275fb-143">RELATED LINKS</span></span>
