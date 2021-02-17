---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 690b00c41aea571786916d2055eb4063c51c4370
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198658"
---
# <span data-ttu-id="60505-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="60505-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="60505-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60505-102">SYNOPSIS</span></span>
<span data-ttu-id="60505-103">Utwórz nowy typ aplikacji sieci szkieletowej usług w ramach określonej grupy zasobów i klastrów.</span><span class="sxs-lookup"><span data-stu-id="60505-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="60505-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="60505-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60505-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="60505-105">DESCRIPTION</span></span>
<span data-ttu-id="60505-106">Polecenie cmdlet tworzy nowy typ aplikacji sieci szkieletowej usługi w ramach określonej grupy zasobów i klastra.</span><span class="sxs-lookup"><span data-stu-id="60505-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="60505-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="60505-107">EXAMPLES</span></span>

### <span data-ttu-id="60505-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="60505-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="60505-109">W tym przykładzie zostanie określony nowy typ aplikacji "testAppType" w grupie zasobów i określonym klastrze.</span><span class="sxs-lookup"><span data-stu-id="60505-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="60505-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60505-110">PARAMETERS</span></span>

### <span data-ttu-id="60505-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="60505-111">-ClusterName</span></span>
<span data-ttu-id="60505-112">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="60505-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60505-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60505-113">-DefaultProfile</span></span>
<span data-ttu-id="60505-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="60505-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60505-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="60505-115">-Name</span></span>
<span data-ttu-id="60505-116">Określanie nazwy typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="60505-116">Specify the name of the application type</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationTypeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60505-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60505-117">-ResourceGroupName</span></span>
<span data-ttu-id="60505-118">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="60505-118">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60505-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60505-119">-Confirm</span></span>
<span data-ttu-id="60505-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="60505-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60505-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60505-121">-WhatIf</span></span>
<span data-ttu-id="60505-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60505-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60505-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="60505-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60505-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60505-124">CommonParameters</span></span>
<span data-ttu-id="60505-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60505-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60505-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60505-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60505-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60505-127">INPUTS</span></span>

### <span data-ttu-id="60505-128">System.String</span><span class="sxs-lookup"><span data-stu-id="60505-128">System.String</span></span>

## <span data-ttu-id="60505-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60505-129">OUTPUTS</span></span>

### <span data-ttu-id="60505-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="60505-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="60505-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="60505-131">NOTES</span></span>

## <span data-ttu-id="60505-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60505-132">RELATED LINKS</span></span>
