---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Enable-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: fcaa5c1342801c4c0ef00e1a4c48abf4a6b4da41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717588"
---
# <span data-ttu-id="07e41-101">Enable-AzureRmHDInsightOperationsManagementSuite</span><span class="sxs-lookup"><span data-stu-id="07e41-101">Enable-AzureRmHDInsightOperationsManagementSuite</span></span>

## <span data-ttu-id="07e41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="07e41-102">SYNOPSIS</span></span>
<span data-ttu-id="07e41-103">Włącza Pakiet Operations Management Suite (OMS) w klastrze usługi HDInsight i odpowiednie dzienniki zostaną wysłane do obszaru roboczego OMS określonego podczas włączania.</span><span class="sxs-lookup"><span data-stu-id="07e41-103">Enables Operations Management Suite (OMS) in a HDInsight cluster and relevant logs will be sent to the OMS workspace specified during enable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07e41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="07e41-104">SYNTAX</span></span>

```
Enable-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-WorkspaceId] <String>
 [-PrimaryKey] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07e41-105">Opis</span><span class="sxs-lookup"><span data-stu-id="07e41-105">DESCRIPTION</span></span>
<span data-ttu-id="07e41-106">Polecenie cmdlet **enable-AzureRmHDInsightOperationsManagementSuite** włącza Pakiet Operations Management Suite (OMS) w klastrze usługi Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="07e41-106">The **Enable-AzureRmHDInsightOperationsManagementSuite** cmdlet enables Operations Management Suite (OMS) in a Azure HDInsight cluster.</span></span>

## <span data-ttu-id="07e41-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="07e41-107">EXAMPLES</span></span>

### <span data-ttu-id="07e41-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="07e41-108">Example 1</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="07e41-109">Pakiet Operations Management Suite (OMS) zostanie włączony w klastrze usługi HDInsight, a odpowiednie dzienniki zostaną wysłane do obszaru roboczego OMS o identyfikatorze 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="07e41-109">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

### <span data-ttu-id="07e41-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="07e41-110">Example 2</span></span>
```
PS C:\> Enable-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>

ErrorInfo  :

State      : Succeeded

RequestId  : 1417ad86-d055-48cd-9d68-a5c19a212a3a

StatusCode : OK
```

<span data-ttu-id="07e41-111">Pakiet Operations Management Suite (OMS) zostanie włączony w klastrze usługi HDInsight, a odpowiednie dzienniki zostaną wysłane do obszaru roboczego OMS o identyfikatorze 1d364e89-bb71-4503-aa3d-a23535aea7bd</span><span class="sxs-lookup"><span data-stu-id="07e41-111">Operations Management Suite (OMS) will be enabled on the HDInsight cluster and relevant logs will be sent to the OMS workspace with id 1d364e89-bb71-4503-aa3d-a23535aea7bd</span></span>

## <span data-ttu-id="07e41-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07e41-112">PARAMETERS</span></span>

### <span data-ttu-id="07e41-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="07e41-113">-Name</span></span>
<span data-ttu-id="07e41-114">Nazwa klastra, w którym ma zostać włączony pakiet Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="07e41-114">The name of the cluster to enable Operations Management Suite(OMS).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07e41-115">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="07e41-115">-PrimaryKey</span></span>
<span data-ttu-id="07e41-116">Klucz podstawowy obszaru roboczego usługi Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="07e41-116">The primary key of the Operations Management Suite(OMS) workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e41-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07e41-117">-ResourceGroupName</span></span>
<span data-ttu-id="07e41-118">Grupa zasobów klastra.</span><span class="sxs-lookup"><span data-stu-id="07e41-118">The resource group of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07e41-119">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="07e41-119">-WorkspaceId</span></span>
<span data-ttu-id="07e41-120">Identyfikator obszaru roboczego usługi Operations Management Suite (OMS).</span><span class="sxs-lookup"><span data-stu-id="07e41-120">The id of the Operations Management Suite(OMS) workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07e41-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="07e41-121">-Confirm</span></span>
<span data-ttu-id="07e41-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07e41-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07e41-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07e41-123">-DefaultProfile</span></span>
<span data-ttu-id="07e41-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="07e41-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07e41-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07e41-125">-WhatIf</span></span>
<span data-ttu-id="07e41-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07e41-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="07e41-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="07e41-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07e41-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07e41-128">CommonParameters</span></span>
<span data-ttu-id="07e41-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07e41-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07e41-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07e41-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07e41-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07e41-131">INPUTS</span></span>

### <span data-ttu-id="07e41-132">System. String</span><span class="sxs-lookup"><span data-stu-id="07e41-132">System.String</span></span>

## <span data-ttu-id="07e41-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="07e41-133">OUTPUTS</span></span>

### <span data-ttu-id="07e41-134">Microsoft. Azure. Management. HDInsight. MODELES. OperationResource</span><span class="sxs-lookup"><span data-stu-id="07e41-134">Microsoft.Azure.Management.HDInsight.Models.OperationResource</span></span>

## <span data-ttu-id="07e41-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="07e41-135">NOTES</span></span>

## <span data-ttu-id="07e41-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07e41-136">RELATED LINKS</span></span>

