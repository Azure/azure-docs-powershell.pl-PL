---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Get-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 645981bb7b2cb02a4bb54a03ccbb570ec31925dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553758"
---
# <span data-ttu-id="e4d31-101">Get-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e4d31-101">Get-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="e4d31-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4d31-102">SYNOPSIS</span></span>
<span data-ttu-id="e4d31-103">Pobieranie szczegółów zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="e4d31-103">Get the cluster resource details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4d31-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4d31-104">SYNTAX</span></span>

```
Get-AzureRmServiceFabricCluster [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4d31-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e4d31-105">DESCRIPTION</span></span>
<span data-ttu-id="e4d31-106">**Dodatek Add-AzureRmServiceFabricCluster** wyświetli dane zasobu klastra.</span><span class="sxs-lookup"><span data-stu-id="e4d31-106">The **Add-AzureRmServiceFabricCluster** will get the cluster resource details.</span></span>

## <span data-ttu-id="e4d31-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4d31-107">EXAMPLES</span></span>

### <span data-ttu-id="e4d31-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e4d31-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceFabricCluster -ResourceGroupName 'Group1' -ClusterName 'Contoso01SFCluster'
```

<span data-ttu-id="e4d31-109">To polecenie spowoduje pobranie szczegółów zasobu klastra dotyczących klastra.</span><span class="sxs-lookup"><span data-stu-id="e4d31-109">This command will get the cluster resource details for cluster 'myCluster'.</span></span>

## <span data-ttu-id="e4d31-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4d31-110">PARAMETERS</span></span>

### <span data-ttu-id="e4d31-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4d31-111">-Name</span></span>
<span data-ttu-id="e4d31-112">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="e4d31-112">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4d31-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4d31-113">-ResourceGroupName</span></span>
<span data-ttu-id="e4d31-114">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e4d31-114">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4d31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4d31-115">-DefaultProfile</span></span>
<span data-ttu-id="e4d31-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4d31-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4d31-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4d31-117">CommonParameters</span></span>
<span data-ttu-id="e4d31-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4d31-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4d31-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4d31-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4d31-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4d31-120">INPUTS</span></span>

### <span data-ttu-id="e4d31-121">System. String</span><span class="sxs-lookup"><span data-stu-id="e4d31-121">System.String</span></span>

## <span data-ttu-id="e4d31-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4d31-122">OUTPUTS</span></span>

### <span data-ttu-id="e4d31-123">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. servicefabric. MODELES. PsCluster, Microsoft. Azure. Commands. servicefabric, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e4d31-123">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster, Microsoft.Azure.Commands.ServiceFabric, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e4d31-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4d31-124">NOTES</span></span>

## <span data-ttu-id="e4d31-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4d31-125">RELATED LINKS</span></span>

