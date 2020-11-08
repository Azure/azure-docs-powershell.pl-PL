---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 257421a43c3da11c82316eaf58d2983fe47d5f05
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063431"
---
# <span data-ttu-id="5ebe9-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5ebe9-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="5ebe9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ebe9-102">SYNOPSIS</span></span>
<span data-ttu-id="5ebe9-103">Pobiera szczegóły puli plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="5ebe9-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="5ebe9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ebe9-104">SYNTAX</span></span>

### <span data-ttu-id="5ebe9-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5ebe9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ebe9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ebe9-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ebe9-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ebe9-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5ebe9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5ebe9-108">DESCRIPTION</span></span>
<span data-ttu-id="5ebe9-109">Polecenie cmdlet **Get-AzNetAppFilesPool** pobiera szczegóły puli ANF.</span><span class="sxs-lookup"><span data-stu-id="5ebe9-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="5ebe9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ebe9-110">EXAMPLES</span></span>

### <span data-ttu-id="5ebe9-111">Przykład 1: uzyskiwanie puli ANF</span><span class="sxs-lookup"><span data-stu-id="5ebe9-111">Example 1: Get an ANF pool</span></span>
```
PS C:\>Get-AzAnfPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool"

Output:

Location          : westus2
Id                : /subscriptions/subsID/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool
Name              : MyAnfAccount/MyAnfPool
Type              : Microsoft.NetApp/netAppAccounts/capacityPools
Tags              :
PoolId            : a3a53a09-fd70-37ab-39dc-392a04cba525
Size              : 4398046511104
ServiceLevel      : Premium
ProvisioningState : Succeeded
```

<span data-ttu-id="5ebe9-112">To polecenie pobiera konto o nazwie MyAnfPool z konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="5ebe9-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="5ebe9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ebe9-113">PARAMETERS</span></span>

### <span data-ttu-id="5ebe9-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5ebe9-114">-AccountName</span></span>
<span data-ttu-id="5ebe9-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="5ebe9-115">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ebe9-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="5ebe9-116">-AccountObject</span></span>
<span data-ttu-id="5ebe9-117">Obiekt konta zawierający pulę do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="5ebe9-117">The account object containing the pool to return</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebe9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ebe9-118">-DefaultProfile</span></span>
<span data-ttu-id="5ebe9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ebe9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ebe9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ebe9-120">-Name</span></span>
<span data-ttu-id="5ebe9-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="5ebe9-121">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ebe9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ebe9-122">-ResourceGroupName</span></span>
<span data-ttu-id="5ebe9-123">Grupa zasobów puli ANF</span><span class="sxs-lookup"><span data-stu-id="5ebe9-123">The resource group of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ebe9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ebe9-124">-ResourceId</span></span>
<span data-ttu-id="5ebe9-125">Identyfikator zasobu puli ANF</span><span class="sxs-lookup"><span data-stu-id="5ebe9-125">The resource id of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ebe9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ebe9-126">CommonParameters</span></span>
<span data-ttu-id="5ebe9-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ebe9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ebe9-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ebe9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ebe9-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ebe9-129">INPUTS</span></span>

### <span data-ttu-id="5ebe9-130">System. String</span><span class="sxs-lookup"><span data-stu-id="5ebe9-130">System.String</span></span>

### <span data-ttu-id="5ebe9-131">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="5ebe9-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="5ebe9-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ebe9-132">OUTPUTS</span></span>

### <span data-ttu-id="5ebe9-133">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="5ebe9-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="5ebe9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ebe9-134">NOTES</span></span>

## <span data-ttu-id="5ebe9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ebe9-135">RELATED LINKS</span></span>
