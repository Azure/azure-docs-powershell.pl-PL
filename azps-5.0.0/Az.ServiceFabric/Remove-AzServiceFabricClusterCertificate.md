---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/remove-azservicefabricclustercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Remove-AzServiceFabricClusterCertificate.md
ms.openlocfilehash: 688ee9f8679a427d53319147e7d13fc9e1305277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224830"
---
# <span data-ttu-id="0e073-101">Remove-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="0e073-101">Remove-AzServiceFabricClusterCertificate</span></span>

## <span data-ttu-id="0e073-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e073-102">SYNOPSIS</span></span>
<span data-ttu-id="0e073-103">Usuwanie certyfikatu klastra ze względu na bezpieczeństwo klastra.</span><span class="sxs-lookup"><span data-stu-id="0e073-103">Remove a cluster certificate from being used for cluster security.</span></span>

## <span data-ttu-id="0e073-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e073-104">SYNTAX</span></span>

```
Remove-AzServiceFabricClusterCertificate -Thumbprint <String> [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e073-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e073-105">DESCRIPTION</span></span>
<span data-ttu-id="0e073-106">Użyj polecenie **Remove-AzServiceFabricClusterCertificate** , aby usunąć certyfikat klastra z klastra, o ile jest już używany inny ważny certyfikat, który jest już używany w klastrze.</span><span class="sxs-lookup"><span data-stu-id="0e073-106">Use **Remove-AzServiceFabricClusterCertificate** to remove a cluster certificate from the cluster, as long as there is another valid certificate that is already in use in the cluster.</span></span>

## <span data-ttu-id="0e073-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e073-107">EXAMPLES</span></span>

### <span data-ttu-id="0e073-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e073-108">Example 1</span></span>
```
PS C:\> Remove-AzServiceFabricClusterCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="0e073-109">To polecenie usuwa certyfikat z 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A odcisku palca, który jest używany do zabezpieczeń klastra.</span><span class="sxs-lookup"><span data-stu-id="0e073-109">This command removes the certificate with thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A from being used for cluster security.</span></span>

## <span data-ttu-id="0e073-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e073-110">PARAMETERS</span></span>

### <span data-ttu-id="0e073-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e073-111">-DefaultProfile</span></span>
<span data-ttu-id="0e073-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e073-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e073-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0e073-113">-Name</span></span>
<span data-ttu-id="0e073-114">Określ nazwę klastra.</span><span class="sxs-lookup"><span data-stu-id="0e073-114">Specify the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e073-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e073-115">-ResourceGroupName</span></span>
<span data-ttu-id="0e073-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e073-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="0e073-117">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="0e073-117">-Thumbprint</span></span>
<span data-ttu-id="0e073-118">Określ odcisk palca klastra, który chcesz usunąć.</span><span class="sxs-lookup"><span data-stu-id="0e073-118">Specify the cluster thumbprint which to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e073-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e073-119">-Confirm</span></span>
<span data-ttu-id="0e073-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e073-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e073-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e073-121">-WhatIf</span></span>
<span data-ttu-id="0e073-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e073-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e073-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0e073-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e073-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e073-124">CommonParameters</span></span>
<span data-ttu-id="0e073-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e073-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e073-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e073-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e073-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e073-127">INPUTS</span></span>

### <span data-ttu-id="0e073-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0e073-128">System.String</span></span>

## <span data-ttu-id="0e073-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e073-129">OUTPUTS</span></span>

### <span data-ttu-id="0e073-130">Microsoft. Azure. Commands. servicefabric. MODELES. PSCluster</span><span class="sxs-lookup"><span data-stu-id="0e073-130">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="0e073-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e073-131">NOTES</span></span>

## <span data-ttu-id="0e073-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e073-132">RELATED LINKS</span></span>
