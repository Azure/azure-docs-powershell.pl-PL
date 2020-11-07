---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeUser.md
ms.openlocfilehash: 0ab290934a956282a16d9e2321b2c5ed948f33af
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893270"
---
# <span data-ttu-id="53f95-101">Get-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="53f95-101">Get-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="53f95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53f95-102">SYNOPSIS</span></span>
<span data-ttu-id="53f95-103">Pobiera użytkowników skonfigurowanych dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="53f95-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="53f95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53f95-104">SYNTAX</span></span>

### <span data-ttu-id="53f95-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="53f95-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53f95-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="53f95-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53f95-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="53f95-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53f95-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="53f95-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="53f95-109">Opis</span><span class="sxs-lookup"><span data-stu-id="53f95-109">DESCRIPTION</span></span>
<span data-ttu-id="53f95-110">Polecenie cmdlet **Get-AzDataBoxEdgeUser** wyświetla listę użytkowników, dla których skonfigurowano urządzenie do krawędzi pola danych.</span><span class="sxs-lookup"><span data-stu-id="53f95-110">The **Get-AzDataBoxEdgeUser** cmdlet lists the users configured for a Data Box Edge device.</span></span> <span data-ttu-id="53f95-111">Aby uzyskać szczegółowe informacje o konkretnym użytkowniku, możesz podać nazwę w polu parametry.</span><span class="sxs-lookup"><span data-stu-id="53f95-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="53f95-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53f95-112">EXAMPLES</span></span>

### <span data-ttu-id="53f95-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="53f95-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="53f95-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53f95-114">PARAMETERS</span></span>

### <span data-ttu-id="53f95-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53f95-115">-DefaultProfile</span></span>
<span data-ttu-id="53f95-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53f95-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53f95-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="53f95-117">-DeviceName</span></span>
<span data-ttu-id="53f95-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="53f95-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f95-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="53f95-119">-DeviceObject</span></span>
<span data-ttu-id="53f95-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="53f95-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="53f95-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53f95-121">-Name</span></span>
<span data-ttu-id="53f95-122">Nazwie</span><span class="sxs-lookup"><span data-stu-id="53f95-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f95-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53f95-123">-ResourceGroupName</span></span>
<span data-ttu-id="53f95-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="53f95-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f95-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53f95-125">-ResourceId</span></span>
<span data-ttu-id="53f95-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="53f95-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53f95-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53f95-127">CommonParameters</span></span>
<span data-ttu-id="53f95-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53f95-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53f95-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53f95-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53f95-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53f95-130">INPUTS</span></span>

### <span data-ttu-id="53f95-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="53f95-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="53f95-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53f95-132">OUTPUTS</span></span>

### <span data-ttu-id="53f95-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="53f95-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="53f95-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53f95-134">NOTES</span></span>

## <span data-ttu-id="53f95-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53f95-135">RELATED LINKS</span></span>
