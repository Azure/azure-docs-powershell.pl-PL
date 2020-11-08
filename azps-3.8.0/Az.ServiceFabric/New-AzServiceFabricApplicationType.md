---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabricapplicationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricApplicationType.md
ms.openlocfilehash: 2e878c562c8f60ecebc9b6a43b3980e06fd0e355
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050688"
---
# <span data-ttu-id="e954b-101">New-AzServiceFabricApplicationType</span><span class="sxs-lookup"><span data-stu-id="e954b-101">New-AzServiceFabricApplicationType</span></span>

## <span data-ttu-id="e954b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e954b-102">SYNOPSIS</span></span>
<span data-ttu-id="e954b-103">Utwórz nowy typ aplikacji sieci szkieletowej usług pod określoną grupą zasobów i klastrem.</span><span class="sxs-lookup"><span data-stu-id="e954b-103">Create new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="e954b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e954b-104">SYNTAX</span></span>

```
New-AzServiceFabricApplicationType [-ResourceGroupName] <String> [-ClusterName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e954b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e954b-105">DESCRIPTION</span></span>
<span data-ttu-id="e954b-106">Polecenie cmdlet tworzy nowy typ aplikacji sieci szkieletowej usług pod określoną grupą zasobów i klastrem.</span><span class="sxs-lookup"><span data-stu-id="e954b-106">The cmdlet creates a new service fabric application type under the specified resource group and cluster.</span></span>

## <span data-ttu-id="e954b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e954b-107">EXAMPLES</span></span>

### <span data-ttu-id="e954b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e954b-108">Example 1</span></span>
```powershell
PS C:\> $resourceGroupName = "testRG"
PS C:\> $clusterName = "testCluster"
PS C:\> $appTypeName = "testAppType"
PS C:\> $appType = New-AzServiceFabricApplicationType -ResourceGroupName $resourceGroupName -ClusterName $clusterName -Name $appTypeName -Verbose
```

<span data-ttu-id="e954b-109">W tym przykładzie zostanie utworzony nowy typ aplikacji "testAppType" w obszarze Grupa zasobów i klaster.</span><span class="sxs-lookup"><span data-stu-id="e954b-109">This example will create a new application type "testAppType" under the resource group and cluster specified.</span></span>

## <span data-ttu-id="e954b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e954b-110">PARAMETERS</span></span>

### <span data-ttu-id="e954b-111">-Nazwaklastraname</span><span class="sxs-lookup"><span data-stu-id="e954b-111">-ClusterName</span></span>
<span data-ttu-id="e954b-112">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="e954b-112">Specify the name of the cluster.</span></span>

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

### <span data-ttu-id="e954b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e954b-113">-DefaultProfile</span></span>
<span data-ttu-id="e954b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e954b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e954b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e954b-115">-Name</span></span>
<span data-ttu-id="e954b-116">Określ nazwę typu aplikacji</span><span class="sxs-lookup"><span data-stu-id="e954b-116">Specify the name of the application type</span></span>

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

### <span data-ttu-id="e954b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e954b-117">-ResourceGroupName</span></span>
<span data-ttu-id="e954b-118">Określ nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e954b-118">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="e954b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e954b-119">-Confirm</span></span>
<span data-ttu-id="e954b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e954b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e954b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e954b-121">-WhatIf</span></span>
<span data-ttu-id="e954b-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e954b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e954b-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e954b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e954b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e954b-124">CommonParameters</span></span>
<span data-ttu-id="e954b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e954b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e954b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e954b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e954b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e954b-127">INPUTS</span></span>

### <span data-ttu-id="e954b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e954b-128">System.String</span></span>

## <span data-ttu-id="e954b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e954b-129">OUTPUTS</span></span>

### <span data-ttu-id="e954b-130">Microsoft. Azure. Commands. servicefabric. MODELES. PSApplicationType</span><span class="sxs-lookup"><span data-stu-id="e954b-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSApplicationType</span></span>

## <span data-ttu-id="e954b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e954b-131">NOTES</span></span>

## <span data-ttu-id="e954b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e954b-132">RELATED LINKS</span></span>
