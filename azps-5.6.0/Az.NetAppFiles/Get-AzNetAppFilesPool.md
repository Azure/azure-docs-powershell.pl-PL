---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 546364e96f7beed16ae8786dc3aaacbf9a84454d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968618"
---
# <span data-ttu-id="965d7-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="965d7-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="965d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="965d7-102">SYNOPSIS</span></span>
<span data-ttu-id="965d7-103">Pobiera szczegółowe informacje o puli plików ANF (Azure NetApp Files).</span><span class="sxs-lookup"><span data-stu-id="965d7-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="965d7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="965d7-104">SYNTAX</span></span>

### <span data-ttu-id="965d7-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="965d7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="965d7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="965d7-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="965d7-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="965d7-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="965d7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="965d7-108">DESCRIPTION</span></span>
<span data-ttu-id="965d7-109">Polecenie **cmdlet Get-AzNetAppFilesPool** pobiera szczegółowe informacje dotyczące puli ANF.</span><span class="sxs-lookup"><span data-stu-id="965d7-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="965d7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="965d7-110">EXAMPLES</span></span>

### <span data-ttu-id="965d7-111">Przykład 1. Uzyskiwanie puli ANF</span><span class="sxs-lookup"><span data-stu-id="965d7-111">Example 1: Get an ANF pool</span></span>
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
TotalThroughputMibps: 262.144
UtilizedThroughputMibps: 164.221
QosType           : Auto
ProvisioningState : Succeeded
```

<span data-ttu-id="965d7-112">To polecenie pobiera konto o nazwie MyAnfPool z konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="965d7-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="965d7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="965d7-113">PARAMETERS</span></span>

### <span data-ttu-id="965d7-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="965d7-114">-AccountName</span></span>
<span data-ttu-id="965d7-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="965d7-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="965d7-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="965d7-116">-AccountObject</span></span>
<span data-ttu-id="965d7-117">Obiekt konta zawierający pulę do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="965d7-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="965d7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="965d7-118">-DefaultProfile</span></span>
<span data-ttu-id="965d7-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="965d7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="965d7-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="965d7-120">-Name</span></span>
<span data-ttu-id="965d7-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="965d7-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="965d7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="965d7-122">-ResourceGroupName</span></span>
<span data-ttu-id="965d7-123">Grupa zasobów puli ANF</span><span class="sxs-lookup"><span data-stu-id="965d7-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="965d7-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="965d7-124">-ResourceId</span></span>
<span data-ttu-id="965d7-125">Identyfikator zasobu puli ANF</span><span class="sxs-lookup"><span data-stu-id="965d7-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="965d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="965d7-126">CommonParameters</span></span>
<span data-ttu-id="965d7-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="965d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="965d7-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="965d7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="965d7-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="965d7-129">INPUTS</span></span>

### <span data-ttu-id="965d7-130">System.String</span><span class="sxs-lookup"><span data-stu-id="965d7-130">System.String</span></span>

### <span data-ttu-id="965d7-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="965d7-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="965d7-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="965d7-132">OUTPUTS</span></span>

### <span data-ttu-id="965d7-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="965d7-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="965d7-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="965d7-134">NOTES</span></span>

## <span data-ttu-id="965d7-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="965d7-135">RELATED LINKS</span></span>
