---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: fdadfde6c798bf404d1f99dbb1ff2a8109d41f73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709741"
---
# <span data-ttu-id="9fc83-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9fc83-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="9fc83-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9fc83-102">SYNOPSIS</span></span>
<span data-ttu-id="9fc83-103">Tworzy nową pulę plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="9fc83-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="9fc83-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9fc83-104">SYNTAX</span></span>

### <span data-ttu-id="9fc83-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9fc83-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9fc83-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9fc83-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9fc83-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9fc83-107">DESCRIPTION</span></span>
<span data-ttu-id="9fc83-108">Polecenie cmdlet **New-AzNetAppFilesPool** tworzy pulę ANF.</span><span class="sxs-lookup"><span data-stu-id="9fc83-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="9fc83-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9fc83-109">EXAMPLES</span></span>

### <span data-ttu-id="9fc83-110">Przykład 1. Tworzenie puli ANF</span><span class="sxs-lookup"><span data-stu-id="9fc83-110">Example 1: Create an ANF pool</span></span>
```
PS C:\>New-AzNetAppFilesPool -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -Name "MyAnfPool" -l "westus2" -PoolSize 4398046511104 -ServiceLevel "Premium"

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

<span data-ttu-id="9fc83-111">To polecenie tworzy nową pulę ANF "MyAnfPool" w ramach konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="9fc83-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="9fc83-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9fc83-112">PARAMETERS</span></span>

### <span data-ttu-id="9fc83-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9fc83-113">-AccountName</span></span>
<span data-ttu-id="9fc83-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="9fc83-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="9fc83-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="9fc83-115">-AccountObject</span></span>
<span data-ttu-id="9fc83-116">Konto nowego obiektu puli</span><span class="sxs-lookup"><span data-stu-id="9fc83-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="9fc83-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fc83-117">-DefaultProfile</span></span>
<span data-ttu-id="9fc83-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9fc83-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fc83-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9fc83-119">-Location</span></span>
<span data-ttu-id="9fc83-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="9fc83-120">The location of the resource</span></span>

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

### <span data-ttu-id="9fc83-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9fc83-121">-Name</span></span>
<span data-ttu-id="9fc83-122">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="9fc83-122">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc83-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="9fc83-123">-PoolSize</span></span>
<span data-ttu-id="9fc83-124">Rozmiar puli ANF</span><span class="sxs-lookup"><span data-stu-id="9fc83-124">The size of the ANF pool</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc83-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fc83-125">-ResourceGroupName</span></span>
<span data-ttu-id="9fc83-126">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="9fc83-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="9fc83-127">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="9fc83-127">-ServiceLevel</span></span>
<span data-ttu-id="9fc83-128">Poziom usługi puli ANF</span><span class="sxs-lookup"><span data-stu-id="9fc83-128">The service level of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc83-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="9fc83-129">-Tag</span></span>
<span data-ttu-id="9fc83-130">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="9fc83-130">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fc83-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9fc83-131">-Confirm</span></span>
<span data-ttu-id="9fc83-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fc83-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fc83-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fc83-133">-WhatIf</span></span>
<span data-ttu-id="9fc83-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9fc83-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fc83-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9fc83-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fc83-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fc83-136">CommonParameters</span></span>
<span data-ttu-id="9fc83-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fc83-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9fc83-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fc83-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fc83-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9fc83-139">INPUTS</span></span>

### <span data-ttu-id="9fc83-140">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="9fc83-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="9fc83-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9fc83-141">OUTPUTS</span></span>

### <span data-ttu-id="9fc83-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9fc83-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="9fc83-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9fc83-143">NOTES</span></span>

## <span data-ttu-id="9fc83-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9fc83-144">RELATED LINKS</span></span>
