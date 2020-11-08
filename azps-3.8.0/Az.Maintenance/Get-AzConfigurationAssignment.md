---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzConfigurationAssignment.md
ms.openlocfilehash: 20ca0e52b23ddcabfe14b2bd2fc9ab633f225390
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053191"
---
# <span data-ttu-id="cb040-101">Get-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="cb040-101">Get-AzConfigurationAssignment</span></span>

## <span data-ttu-id="cb040-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb040-102">SYNOPSIS</span></span>
<span data-ttu-id="cb040-103">Lista configurationAssignments dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="cb040-103">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="cb040-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb040-104">SYNTAX</span></span>

```
Get-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb040-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cb040-105">DESCRIPTION</span></span>
<span data-ttu-id="cb040-106">Lista configurationAssignments dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="cb040-106">List configurationAssignments for resource.</span></span>

## <span data-ttu-id="cb040-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb040-107">EXAMPLES</span></span>

### <span data-ttu-id="cb040-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cb040-108">Example 1</span></span>
```powershell
PS C:\> Get-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute


MaintenanceConfigurationId : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/ps1/providers/Microsoft.Maintenance/maintenanceConfigurations/ps2
Id                         :
/subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtestwestus2/providers/Microsoft.Compute/hostGroups/smddhgwestus2/hosts/smddhwestus2/providers/Microsoft.Maintenance/configurationAssignments/ps2
Name                       : ps2
Type                       : Microsoft.Maintenance/configurationAssignments
```

<span data-ttu-id="cb040-109">Lista configurationAssignments dla dedykowanego hosta.</span><span class="sxs-lookup"><span data-stu-id="cb040-109">List configurationAssignments for dedicated host.</span></span>

## <span data-ttu-id="cb040-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb040-110">PARAMETERS</span></span>

### <span data-ttu-id="cb040-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb040-111">-DefaultProfile</span></span>
<span data-ttu-id="cb040-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb040-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb040-113">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="cb040-113">-ProviderName</span></span>
<span data-ttu-id="cb040-114">Nazwa dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb040-114">The resource provider Name.</span></span>

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

### <span data-ttu-id="cb040-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb040-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb040-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cb040-116">The resource Group Name.</span></span>

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

### <span data-ttu-id="cb040-117">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="cb040-117">-ResourceName</span></span>
<span data-ttu-id="cb040-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="cb040-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb040-119">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="cb040-119">-ResourceParentName</span></span>
<span data-ttu-id="cb040-120">Nazwa zasobu nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="cb040-120">The parent resource name.</span></span>

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

### <span data-ttu-id="cb040-121">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="cb040-121">-ResourceParentType</span></span>
<span data-ttu-id="cb040-122">Nadrzędny typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="cb040-122">The parent resource type.</span></span>

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

### <span data-ttu-id="cb040-123">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="cb040-123">-ResourceType</span></span>
<span data-ttu-id="cb040-124">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="cb040-124">The resource type.</span></span>

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

### <span data-ttu-id="cb040-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb040-125">CommonParameters</span></span>
<span data-ttu-id="cb040-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb040-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb040-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb040-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb040-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb040-128">INPUTS</span></span>

### <span data-ttu-id="cb040-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cb040-129">System.String</span></span>

## <span data-ttu-id="cb040-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb040-130">OUTPUTS</span></span>

### <span data-ttu-id="cb040-131">Microsoft. Azure. Commands. Maintenance. models. PSConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="cb040-131">Microsoft.Azure.Commands.Maintenance.Models.PSConfigurationAssignment</span></span>

## <span data-ttu-id="cb040-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb040-132">NOTES</span></span>

## <span data-ttu-id="cb040-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb040-133">RELATED LINKS</span></span>
