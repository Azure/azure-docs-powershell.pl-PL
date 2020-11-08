---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilespool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesPool.md
ms.openlocfilehash: f3b1a6180fb59b3c44942459e09a22a333fc9720
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064004"
---
# <span data-ttu-id="4745c-101">New-AzNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="4745c-101">New-AzNetAppFilesPool</span></span>

## <span data-ttu-id="4745c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4745c-102">SYNOPSIS</span></span>
<span data-ttu-id="4745c-103">Tworzy nową pulę plików usługi Azure NetApp (ANF).</span><span class="sxs-lookup"><span data-stu-id="4745c-103">Creates a new Azure NetApp Files (ANF) pool.</span></span>

## <span data-ttu-id="4745c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4745c-104">SYNTAX</span></span>

### <span data-ttu-id="4745c-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4745c-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesPool -ResourceGroupName <String> -Location <String> -AccountName <String> -Name <String>
 -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4745c-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4745c-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesPool -Name <String> -PoolSize <Int64> -ServiceLevel <String> [-Tag <Hashtable>]
 -AccountObject <PSNetAppFilesAccount> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4745c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4745c-107">DESCRIPTION</span></span>
<span data-ttu-id="4745c-108">Polecenie cmdlet **New-AzNetAppFilesPool** tworzy pulę ANF.</span><span class="sxs-lookup"><span data-stu-id="4745c-108">The **New-AzNetAppFilesPool** cmdlet creates an ANF pool.</span></span>

## <span data-ttu-id="4745c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4745c-109">EXAMPLES</span></span>

### <span data-ttu-id="4745c-110">Przykład 1. Tworzenie puli ANF</span><span class="sxs-lookup"><span data-stu-id="4745c-110">Example 1: Create an ANF pool</span></span>
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

<span data-ttu-id="4745c-111">To polecenie tworzy nową pulę ANF "MyAnfPool" w ramach konta "MyAnfAccount".</span><span class="sxs-lookup"><span data-stu-id="4745c-111">This command creates the new ANF pool "MyAnfPool" within the account "MyAnfAccount".</span></span>

## <span data-ttu-id="4745c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4745c-112">PARAMETERS</span></span>

### <span data-ttu-id="4745c-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4745c-113">-AccountName</span></span>
<span data-ttu-id="4745c-114">Nazwa konta usługi ANF</span><span class="sxs-lookup"><span data-stu-id="4745c-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="4745c-115">-Accountobject</span><span class="sxs-lookup"><span data-stu-id="4745c-115">-AccountObject</span></span>
<span data-ttu-id="4745c-116">Konto nowego obiektu puli</span><span class="sxs-lookup"><span data-stu-id="4745c-116">The account for the new pool object</span></span>

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

### <span data-ttu-id="4745c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4745c-117">-DefaultProfile</span></span>
<span data-ttu-id="4745c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4745c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4745c-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4745c-119">-Location</span></span>
<span data-ttu-id="4745c-120">Lokalizacja zasobu</span><span class="sxs-lookup"><span data-stu-id="4745c-120">The location of the resource</span></span>

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

### <span data-ttu-id="4745c-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4745c-121">-Name</span></span>
<span data-ttu-id="4745c-122">Nazwa puli ANF</span><span class="sxs-lookup"><span data-stu-id="4745c-122">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4745c-123">-PoolSize</span><span class="sxs-lookup"><span data-stu-id="4745c-123">-PoolSize</span></span>
<span data-ttu-id="4745c-124">Rozmiar puli ANF</span><span class="sxs-lookup"><span data-stu-id="4745c-124">The size of the ANF pool</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4745c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4745c-125">-ResourceGroupName</span></span>
<span data-ttu-id="4745c-126">Grupa zasobów konta ANF</span><span class="sxs-lookup"><span data-stu-id="4745c-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="4745c-127">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="4745c-127">-ServiceLevel</span></span>
<span data-ttu-id="4745c-128">Poziom usługi puli ANF</span><span class="sxs-lookup"><span data-stu-id="4745c-128">The service level of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4745c-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="4745c-129">-Tag</span></span>
<span data-ttu-id="4745c-130">Obiekt Hashtable reprezentujący znaczniki zasobów</span><span class="sxs-lookup"><span data-stu-id="4745c-130">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4745c-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4745c-131">-Confirm</span></span>
<span data-ttu-id="4745c-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4745c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4745c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4745c-133">-WhatIf</span></span>
<span data-ttu-id="4745c-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4745c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4745c-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4745c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4745c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4745c-136">CommonParameters</span></span>
<span data-ttu-id="4745c-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4745c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4745c-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4745c-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4745c-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4745c-139">INPUTS</span></span>

### <span data-ttu-id="4745c-140">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesAccount</span><span class="sxs-lookup"><span data-stu-id="4745c-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesAccount</span></span>

## <span data-ttu-id="4745c-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4745c-141">OUTPUTS</span></span>

### <span data-ttu-id="4745c-142">Microsoft. Azure. Commands. NetAppFiles. models. PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="4745c-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="4745c-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4745c-143">NOTES</span></span>

## <span data-ttu-id="4745c-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4745c-144">RELATED LINKS</span></span>
