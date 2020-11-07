---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesPool.md
ms.openlocfilehash: 56613276907772cfe3f2cbd99810ff247485913f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870955"
---
# <span data-ttu-id="d653f-101">Get-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d653f-101">Get-AzNetAppFilesPool</span></span>

## <span data-ttu-id="d653f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d653f-102">SYNOPSIS</span></span>
<span data-ttu-id="d653f-103">Pobiera szczegóły puli plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="d653f-103">Gets details of an Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="d653f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d653f-104">SYNTAX</span></span>

### <span data-ttu-id="d653f-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d653f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesPool -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d653f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d653f-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesPool -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d653f-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d653f-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesPool -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d653f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d653f-108">DESCRIPTION</span></span>
<span data-ttu-id="d653f-109">Polecenie cmdlet **Get-AzNetAppFilesPool** pobiera szczegóły puli ANF.</span><span class="sxs-lookup"><span data-stu-id="d653f-109">The **Get-AzNetAppFilesPool** cmdlet gets details of an ANF pool.</span></span>

## <span data-ttu-id="d653f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d653f-110">EXAMPLES</span></span>

### <span data-ttu-id="d653f-111">Przykład 1: uzyskiwanie puli ANF</span><span class="sxs-lookup"><span data-stu-id="d653f-111">Example 1: Get an ANF pool</span></span>
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

<span data-ttu-id="d653f-112">To polecenie pobiera konto o nazwie MyAnfPool z konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="d653f-112">This command gets the account named MyAnfPool from the account "MyAnfAccount".</span></span>

## <span data-ttu-id="d653f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d653f-113">PARAMETERS</span></span>

### <span data-ttu-id="d653f-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d653f-114">-AccountName</span></span>
<span data-ttu-id="d653f-115">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="d653f-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d653f-116">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="d653f-116">-AccountObject</span></span>
<span data-ttu-id="d653f-117">Obiekt konta zawierający pulę do zwrócenia</span><span class="sxs-lookup"><span data-stu-id="d653f-117">The account object containing the pool to return</span></span>

```yaml
Type: PSNetAppFilesAccount
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d653f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d653f-118">-DefaultProfile</span></span>
<span data-ttu-id="d653f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d653f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d653f-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d653f-120">-Name</span></span>
<span data-ttu-id="d653f-121">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="d653f-121">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases: PoolName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d653f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d653f-122">-ResourceGroupName</span></span>
<span data-ttu-id="d653f-123">Grupa zasobów puli ANF</span><span class="sxs-lookup"><span data-stu-id="d653f-123">The resource group of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d653f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d653f-124">-ResourceId</span></span>
<span data-ttu-id="d653f-125">Identyfikator zasobu puli ANF</span><span class="sxs-lookup"><span data-stu-id="d653f-125">The resource id of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d653f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d653f-126">CommonParameters</span></span>
<span data-ttu-id="d653f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d653f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d653f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d653f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d653f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d653f-129">INPUTS</span></span>

### <span data-ttu-id="d653f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d653f-130">System.String</span></span>

### <span data-ttu-id="d653f-131">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="d653f-131">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="d653f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d653f-132">OUTPUTS</span></span>

### <span data-ttu-id="d653f-133">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="d653f-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="d653f-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d653f-134">NOTES</span></span>

## <span data-ttu-id="d653f-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d653f-135">RELATED LINKS</span></span>
