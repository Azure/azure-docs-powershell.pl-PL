---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/remove-azurermservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/Remove-AzureRmServiceFabricClusterCertificate.md
ms.openlocfilehash: f99d4df206bff962c1cd44a93f1e1ea04aad7740
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526578"
---
# <span data-ttu-id="eb017-101">Remove-AzureRmServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="eb017-101">Remove-AzureRmServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="eb017-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb017-102">SYNOPSIS</span></span>
<span data-ttu-id="eb017-103">Usuwanie certyfikatu klastra ze względu na bezpieczeństwo klastra.</span><span class="sxs-lookup"><span data-stu-id="eb017-103">Remove a cluster certificate from being used for cluster security.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb017-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb017-104">SYNTAX</span></span>

```
Remove-AzureRmServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eb017-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eb017-105">DESCRIPTION</span></span>
<span data-ttu-id="eb017-106">Użyj polecenie **Remove-AzureRmServiceFabricClusterCertificate** , aby usunąć certyfikat klastra z klastra, o ile jest już używany inny ważny certyfikat, który jest już używany w klastrze.</span><span class="sxs-lookup"><span data-stu-id="eb017-106">Use **Remove-AzureRmServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="eb017-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb017-107">EXAMPLES</span></span>

### <span data-ttu-id="eb017-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eb017-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="eb017-109">To polecenie usuwa certyfikat z 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A odcisku palca, który jest używany do zabezpieczeń klastra.</span><span class="sxs-lookup"><span data-stu-id="eb017-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="eb017-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb017-110">PARAMETERS</span></span>

### <span data-ttu-id="eb017-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb017-111">-DefaultProfile</span></span>
<span data-ttu-id="eb017-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb017-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb017-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="eb017-113">-Name</span></span>
<span data-ttu-id="eb017-114">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="eb017-114">Specify the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb017-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb017-115">-ResourceGroupName</span></span>
<span data-ttu-id="eb017-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eb017-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb017-117">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="eb017-117">-Thumbprint</span></span>
<span data-ttu-id="eb017-118">Określ odcisk palca klastra, który chcesz usunąć.</span><span class="sxs-lookup"><span data-stu-id="eb017-118">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb017-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb017-119">-Confirm</span></span>
<span data-ttu-id="eb017-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb017-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb017-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb017-121">-WhatIf</span></span>
<span data-ttu-id="eb017-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb017-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eb017-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eb017-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb017-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb017-124">CommonParameters</span></span>
<span data-ttu-id="eb017-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb017-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb017-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb017-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb017-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb017-127">INPUTS</span></span>

### <span data-ttu-id="eb017-128">System. String</span><span class="sxs-lookup"><span data-stu-id="eb017-128">System.String</span></span>

## <span data-ttu-id="eb017-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb017-129">OUTPUTS</span></span>

### <span data-ttu-id="eb017-130">Microsoft. Azure. Commands. servicefabric. MODELES. PsCluster</span><span class="sxs-lookup"><span data-stu-id="eb017-130">Microsoft.Azure.Commands.ServiceFabric.Models.PsCluster</span></span>

## <span data-ttu-id="eb017-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb017-131">NOTES</span></span>

## <span data-ttu-id="eb017-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb017-132">RELATED LINKS</span></span>

