---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: d41ce912761770d724fd700249f07d0af11c9647
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187274"
---
# <span data-ttu-id="20257-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="20257-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="20257-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20257-102">SYNOPSIS</span></span>
<span data-ttu-id="20257-103">Pobiera szczegółowe informacje o puli plików ANF (Azure NetApp Files).</span><span class="sxs-lookup"><span data-stu-id="20257-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="20257-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="20257-104">SYNTAX</span></span>

### <span data-ttu-id="20257-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="20257-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20257-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20257-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20257-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20257-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20257-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="20257-108">DESCRIPTION</span></span>
<span data-ttu-id="20257-109">Polecenie **cmdlet Get-AzNetAppFilesPool** pobiera szczegółowe informacje dotyczące puli ANF.</span><span class="sxs-lookup"><span data-stu-id="20257-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="20257-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="20257-110">EXAMPLES</span></span>

### <span data-ttu-id="20257-111">Przykład 1. Uzyskiwanie puli ANF</span><span class="sxs-lookup"><span data-stu-id="20257-111">Example 1: Get an ANF pool</span></span>
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

<span data-ttu-id="20257-112">To polecenie pobiera konto o nazwie MyAnfPool z konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="20257-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="20257-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20257-113">PARAMETERS</span></span>

### <span data-ttu-id="20257-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="20257-114">-AccountName</span></span>
<span data-ttu-id="20257-115">Nazwa konta ANF</span><span class="sxs-lookup"><span data-stu-id="20257-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="20257-116">-AccountObject</span><span class="sxs-lookup"><span data-stu-id="20257-116">-AccountObject</span></span>
<span data-ttu-id="20257-117">Obiekt konta zawierający pulę do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="20257-117">The account object containing the pool to return</span></span>

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

### <span data-ttu-id="20257-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20257-118">-DefaultProfile</span></span>
<span data-ttu-id="20257-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="20257-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20257-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="20257-120">-Name</span></span>
<span data-ttu-id="20257-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="20257-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="20257-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20257-122">-ResourceGroupName</span></span>
<span data-ttu-id="20257-123">Grupa zasobów puli ANF</span><span class="sxs-lookup"><span data-stu-id="20257-123">The resource group of the ANF pool</span></span>

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

### <span data-ttu-id="20257-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20257-124">-ResourceId</span></span>
<span data-ttu-id="20257-125">Identyfikator zasobu puli ANF</span><span class="sxs-lookup"><span data-stu-id="20257-125">The resource id of the ANF pool</span></span>

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

### <span data-ttu-id="20257-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20257-126">CommonParameters</span></span>
<span data-ttu-id="20257-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20257-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20257-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20257-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20257-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20257-129">INPUTS</span></span>

### <span data-ttu-id="20257-130">System.String</span><span class="sxs-lookup"><span data-stu-id="20257-130">System.String</span></span>

### <span data-ttu-id="20257-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="20257-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="20257-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20257-132">OUTPUTS</span></span>

### <span data-ttu-id="20257-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="20257-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="20257-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="20257-134">NOTES</span></span>

## <span data-ttu-id="20257-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20257-135">RELATED LINKS</span></span>
