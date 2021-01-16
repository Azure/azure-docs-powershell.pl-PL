---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeUser.md
ms.openlocfilehash: 3a9945d94b1aec3e82d4d79d09df0bacb3b3a11d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333826"
---
# <span data-ttu-id="06e36-101">Get-AzStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="06e36-101">Get-AzStackEdgeUser</span></span>

## <span data-ttu-id="06e36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06e36-102">SYNOPSIS</span></span>
<span data-ttu-id="06e36-103">Pobiera użytkowników skonfigurowanych dla urządzenia.</span><span class="sxs-lookup"><span data-stu-id="06e36-103">Gets the configured users for a device.</span></span>

## <span data-ttu-id="06e36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06e36-104">SYNTAX</span></span>

### <span data-ttu-id="06e36-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="06e36-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06e36-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="06e36-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeUser -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06e36-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="06e36-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06e36-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="06e36-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeUser [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="06e36-109">Opis</span><span class="sxs-lookup"><span data-stu-id="06e36-109">DESCRIPTION</span></span>
<span data-ttu-id="06e36-110">Polecenie cmdlet **Get-AzStackEdgeUser** wyświetla listę użytkowników skonfigurowanych dla urządzenia z krawędzią stosu.</span><span class="sxs-lookup"><span data-stu-id="06e36-110">The **Get-AzStackEdgeUser** cmdlet lists the users configured for a Stack Edge device.</span></span> <span data-ttu-id="06e36-111">Aby uzyskać szczegółowe informacje o konkretnym użytkowniku, możesz podać nazwę w polu parametry.</span><span class="sxs-lookup"><span data-stu-id="06e36-111">You can mention the Name in parameters to get details about a specific user.</span></span>

## <span data-ttu-id="06e36-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06e36-112">EXAMPLES</span></span>

### <span data-ttu-id="06e36-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06e36-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName
User name  Type  ResourceGroupName DeviceName
---------  ----  ----------------- ----------
deviceName Share resourceGroupName deviceName
```

## <span data-ttu-id="06e36-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06e36-114">PARAMETERS</span></span>

### <span data-ttu-id="06e36-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e36-115">-DefaultProfile</span></span>
<span data-ttu-id="06e36-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06e36-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06e36-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="06e36-117">-DeviceName</span></span>
<span data-ttu-id="06e36-118">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="06e36-118">Device Name</span></span>

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

### <span data-ttu-id="06e36-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="06e36-119">-DeviceObject</span></span>
<span data-ttu-id="06e36-120">Podaj odpowiedni obiekt urządzenia</span><span class="sxs-lookup"><span data-stu-id="06e36-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="06e36-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06e36-121">-Name</span></span>
<span data-ttu-id="06e36-122">Nazwie</span><span class="sxs-lookup"><span data-stu-id="06e36-122">Username</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: Username

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: Username

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e36-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e36-123">-ResourceGroupName</span></span>
<span data-ttu-id="06e36-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="06e36-124">Resource Group Name</span></span>

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

### <span data-ttu-id="06e36-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06e36-125">-ResourceId</span></span>
<span data-ttu-id="06e36-126">Identyfikator zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="06e36-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="06e36-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e36-127">CommonParameters</span></span>
<span data-ttu-id="06e36-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06e36-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e36-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06e36-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e36-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06e36-130">INPUTS</span></span>

### <span data-ttu-id="06e36-131">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="06e36-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="06e36-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06e36-132">OUTPUTS</span></span>

### <span data-ttu-id="06e36-133">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeUser</span><span class="sxs-lookup"><span data-stu-id="06e36-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeUser</span></span>

## <span data-ttu-id="06e36-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06e36-134">NOTES</span></span>

## <span data-ttu-id="06e36-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06e36-135">RELATED LINKS</span></span>
