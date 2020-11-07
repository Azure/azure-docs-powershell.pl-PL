---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
ms.openlocfilehash: dc8b22697d606e827a0855a446d969ff2c90edc8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707167"
---
# <span data-ttu-id="dc1bd-101">Remove-AzAks</span><span class="sxs-lookup"><span data-stu-id="dc1bd-101">Remove-AzAks</span></span>

## <span data-ttu-id="dc1bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc1bd-102">SYNOPSIS</span></span>
<span data-ttu-id="dc1bd-103">Usuń zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="dc1bd-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="dc1bd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc1bd-104">SYNTAX</span></span>

### <span data-ttu-id="dc1bd-105">GroupNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dc1bd-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc1bd-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc1bd-106">InputObjectParameterSet</span></span>
```
Remove-AzAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc1bd-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc1bd-107">IdParameterSet</span></span>
```
Remove-AzAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc1bd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dc1bd-108">DESCRIPTION</span></span>
<span data-ttu-id="dc1bd-109">Usuń zarządzany klaster Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="dc1bd-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="dc1bd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc1bd-110">EXAMPLES</span></span>

### <span data-ttu-id="dc1bd-111">Usuwanie istniejącego klastra zarządzanego Kubernetes</span><span class="sxs-lookup"><span data-stu-id="dc1bd-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="dc1bd-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc1bd-112">PARAMETERS</span></span>

### <span data-ttu-id="dc1bd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc1bd-113">-AsJob</span></span>
<span data-ttu-id="dc1bd-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="dc1bd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc1bd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc1bd-115">-DefaultProfile</span></span>
<span data-ttu-id="dc1bd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc1bd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc1bd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dc1bd-117">-Force</span></span>
<span data-ttu-id="dc1bd-118">Usuwanie zarządzanego klastra Kubernetes bez monitowania</span><span class="sxs-lookup"><span data-stu-id="dc1bd-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="dc1bd-119">-ID</span><span class="sxs-lookup"><span data-stu-id="dc1bd-119">-Id</span></span>
<span data-ttu-id="dc1bd-120">Identyfikator zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="dc1bd-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="dc1bd-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dc1bd-121">-InputObject</span></span>
<span data-ttu-id="dc1bd-122">Obiekt PSKubernetesCluster, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="dc1bd-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="dc1bd-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc1bd-123">-Name</span></span>
<span data-ttu-id="dc1bd-124">Nazwa zarządzanego klastra Kubernetes</span><span class="sxs-lookup"><span data-stu-id="dc1bd-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="dc1bd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc1bd-125">-PassThru</span></span>
<span data-ttu-id="dc1bd-126">Zwraca wartość PRAWDA, Jeśli usunięcie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="dc1bd-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="dc1bd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc1bd-127">-ResourceGroupName</span></span>
<span data-ttu-id="dc1bd-128">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dc1bd-128">Resource group name</span></span>

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

### <span data-ttu-id="dc1bd-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc1bd-129">-Confirm</span></span>
<span data-ttu-id="dc1bd-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc1bd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc1bd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc1bd-131">-WhatIf</span></span>
<span data-ttu-id="dc1bd-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc1bd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc1bd-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dc1bd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc1bd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc1bd-134">CommonParameters</span></span>
<span data-ttu-id="dc1bd-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc1bd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc1bd-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc1bd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc1bd-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc1bd-137">INPUTS</span></span>

### <span data-ttu-id="dc1bd-138">Microsoft. Azure. Commands. AKS. models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="dc1bd-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="dc1bd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="dc1bd-139">System.String</span></span>

## <span data-ttu-id="dc1bd-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc1bd-140">OUTPUTS</span></span>

### <span data-ttu-id="dc1bd-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="dc1bd-141">System.Boolean</span></span>

## <span data-ttu-id="dc1bd-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc1bd-142">NOTES</span></span>

## <span data-ttu-id="dc1bd-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc1bd-143">RELATED LINKS</span></span>
