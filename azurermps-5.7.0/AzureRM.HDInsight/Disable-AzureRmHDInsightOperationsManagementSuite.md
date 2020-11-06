---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/disable-azurermhdinsightoperationsmanagementsuite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Disable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: c29c27ab7b2212670abf7e100678cdfdd5beb6cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548116"
---
# <span data-ttu-id="5ed87-101">Disable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="5ed87-101">Disable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="5ed87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ed87-102">SYNOPSIS</span></span>
<span data-ttu-id="5ed87-103">Wyłącza Pakiet Operations Management Suite (OMS) w klastrze usługi HDInsight i odpowiednie dzienniki przestaną przepływ na obszar roboczy OMS określony podczas włączania.</span><span class="sxs-lookup"><span data-stu-id="5ed87-103">Disables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will stop flowing to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ed87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ed87-104">SYNTAX</span></span>

```
Disable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ed87-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ed87-105">DESCRIPTION</span></span>
<span data-ttu-id="5ed87-106">Polecenie cmdlet **disable-AzureRmHDInsightOperationsManagementSuite** wyłącza Pakiet Operations Management Suite (OMS) w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5ed87-106">The **Disable-AzureRmHDInsightOperationsManagementSuite** cmdlet disables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5ed87-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ed87-107">EXAMPLES</span></span>

### <span data-ttu-id="5ed87-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ed87-108">Example 1</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="5ed87-109">Pakiet Operations Management Suite (OMS) zostanie wyłączony w klastrze usługi HDInsight, a odpowiednie dzienniki zakończą przepływ do obszaru roboczego OMS.</span><span class="sxs-lookup"><span data-stu-id="5ed87-109">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

### <span data-ttu-id="5ed87-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5ed87-110">Example 2</span></span>
```
PS C:\> Disable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="5ed87-111">Pakiet Operations Management Suite (OMS) zostanie wyłączony w klastrze usługi HDInsight, a odpowiednie dzienniki zakończą przepływ do obszaru roboczego OMS.</span><span class="sxs-lookup"><span data-stu-id="5ed87-111">Operations Management Suite (OMS) will be disabled on the HDInsight cluster and relevant logs will stop flowing to the OMS workspace.</span></span>

## <span data-ttu-id="5ed87-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ed87-112">PARAMETERS</span></span>

### <span data-ttu-id="5ed87-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ed87-113">-DefaultProfile</span></span>
<span data-ttu-id="5ed87-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5ed87-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ed87-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ed87-115">-Name</span></span>
<span data-ttu-id="5ed87-116">Nazwa klastra, aby wyłączyć Pakiet Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="5ed87-116">The name of the cluster to disable Operations Management Suite(OMS).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed87-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ed87-117">-ResourceGroupName</span></span>
<span data-ttu-id="5ed87-118">Grupa zasobów klastra.</span><span class="sxs-lookup"><span data-stu-id="5ed87-118">The resource group of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ed87-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ed87-119">-Confirm</span></span>
<span data-ttu-id="5ed87-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ed87-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ed87-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ed87-121">-WhatIf</span></span>
<span data-ttu-id="5ed87-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ed87-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ed87-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ed87-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ed87-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ed87-124">CommonParameters</span></span>
<span data-ttu-id="5ed87-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ed87-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ed87-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ed87-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ed87-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ed87-127">INPUTS</span></span>

### <span data-ttu-id="5ed87-128">System. String</span><span class="sxs-lookup"><span data-stu-id="5ed87-128">System.String</span></span>

## <span data-ttu-id="5ed87-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ed87-129">OUTPUTS</span></span>

### <span data-ttu-id="5ed87-130">Microsoft. Azure. Management. HDInsight. MODELES. OperationResource</span><span class="sxs-lookup"><span data-stu-id="5ed87-130">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="5ed87-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ed87-131">NOTES</span></span>

## <span data-ttu-id="5ed87-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ed87-132">RELATED LINKS</span></span>

