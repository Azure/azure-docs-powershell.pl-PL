---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeShare.md
ms.openlocfilehash: 0e0d0e3b2dfca824d66a9a75f3e22438335c97db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050025"
---
# <span data-ttu-id="5e6a7-101">Get-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5e6a7-101">Get-AzStackEdgeShare</span></span>

## <span data-ttu-id="5e6a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e6a7-103">Pobiera dostępne akcje dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="5e6a7-103">Gets the available shares for a device.</span></span>

## <span data-ttu-id="5e6a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e6a7-104">SYNTAX</span></span>

### <span data-ttu-id="5e6a7-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5e6a7-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e6a7-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e6a7-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e6a7-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e6a7-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e6a7-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e6a7-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeShare [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="5e6a7-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5e6a7-109">DESCRIPTION</span></span>
<span data-ttu-id="5e6a7-110">Polecenie cmdlet **Get-AzStackEdgeShare** Pobiera dostępne akcje dla urządzenia ze stosem.</span><span class="sxs-lookup"><span data-stu-id="5e6a7-110">The **Get-AzStackEdgeShare** cmdlet gets the available shares for a Stack Edge device.</span></span> <span data-ttu-id="5e6a7-111">Jeśli zostanie podana nazwa, otrzymasz nazwę Udostępnij.</span><span class="sxs-lookup"><span data-stu-id="5e6a7-111">If Name is provided this will get the share by Name.</span></span>

## <span data-ttu-id="5e6a7-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e6a7-112">EXAMPLES</span></span>

### <span data-ttu-id="5e6a7-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e6a7-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName
Name       Type       DataPolicy       DataFormat       ResourceGroupName     StorageAccountName
---------- ---------- ---------------- ---------------- --------------------- -------------------
share-1    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-2    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-3    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
share-4    SMB        Cloud            PageBlob         resourceGroupName     storageAccountName
```

## <span data-ttu-id="5e6a7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e6a7-114">PARAMETERS</span></span>

### <span data-ttu-id="5e6a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e6a7-115">-DefaultProfile</span></span>
<span data-ttu-id="5e6a7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e6a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e6a7-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="5e6a7-117">-DeviceName</span></span>
<span data-ttu-id="5e6a7-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="5e6a7-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e6a7-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="5e6a7-119">-DeviceObject</span></span>
<span data-ttu-id="5e6a7-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="5e6a7-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e6a7-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5e6a7-121">-Name</span></span>
<span data-ttu-id="5e6a7-122">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="5e6a7-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: EdgeShareName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e6a7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e6a7-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e6a7-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5e6a7-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e6a7-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e6a7-125">-ResourceId</span></span>
<span data-ttu-id="5e6a7-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5e6a7-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e6a7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e6a7-127">CommonParameters</span></span>
<span data-ttu-id="5e6a7-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e6a7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e6a7-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e6a7-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e6a7-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e6a7-130">INPUTS</span></span>

### <span data-ttu-id="5e6a7-131">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5e6a7-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="5e6a7-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e6a7-132">OUTPUTS</span></span>

### <span data-ttu-id="5e6a7-133">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="5e6a7-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="5e6a7-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e6a7-134">NOTES</span></span>

## <span data-ttu-id="5e6a7-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e6a7-135">RELATED LINKS</span></span>
