---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052023"
---
# <span data-ttu-id="3a3c0-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a3c0-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="3a3c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a3c0-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3c0-103">Tworzy nowy kontener magazynu na stronie konta magazynu Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="3a3c0-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="3a3c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a3c0-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a3c0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3a3c0-105">DESCRIPTION</span></span>
<span data-ttu-id="3a3c0-106">Polecenie cmdlet **New-AzStackEdgeStorageContainer** tworzy nowy kontener magazynu na stronie konta magazynu Edge na urządzeniu z krawędziami stosu.</span><span class="sxs-lookup"><span data-stu-id="3a3c0-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="3a3c0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a3c0-107">EXAMPLES</span></span>

### <span data-ttu-id="3a3c0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a3c0-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="3a3c0-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a3c0-109">PARAMETERS</span></span>

### <span data-ttu-id="3a3c0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a3c0-110">-AsJob</span></span>
<span data-ttu-id="3a3c0-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="3a3c0-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a3c0-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="3a3c0-112">-DataFormat</span></span>
<span data-ttu-id="3a3c0-113">Ustaw format danych: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="3a3c0-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="3a3c0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3c0-114">-DefaultProfile</span></span>
<span data-ttu-id="3a3c0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a3c0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a3c0-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3a3c0-116">-DeviceName</span></span>
<span data-ttu-id="3a3c0-117">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="3a3c0-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3c0-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3a3c0-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="3a3c0-119">Podaj nazwę istniejącego EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3a3c0-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3c0-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a3c0-120">-Name</span></span>
<span data-ttu-id="3a3c0-121">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="3a3c0-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a3c0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3c0-122">-ResourceGroupName</span></span>
<span data-ttu-id="3a3c0-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3a3c0-123">Resource Group Name</span></span>

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

### <span data-ttu-id="3a3c0-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a3c0-124">-Confirm</span></span>
<span data-ttu-id="3a3c0-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a3c0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a3c0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a3c0-126">-WhatIf</span></span>
<span data-ttu-id="3a3c0-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a3c0-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a3c0-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a3c0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a3c0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3c0-129">CommonParameters</span></span>
<span data-ttu-id="3a3c0-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a3c0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3c0-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3a3c0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3c0-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a3c0-132">INPUTS</span></span>

### <span data-ttu-id="3a3c0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="3a3c0-133">System.String</span></span>

## <span data-ttu-id="3a3c0-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a3c0-134">OUTPUTS</span></span>

### <span data-ttu-id="3a3c0-135">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3a3c0-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="3a3c0-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a3c0-136">NOTES</span></span>

## <span data-ttu-id="3a3c0-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a3c0-137">RELATED LINKS</span></span>
