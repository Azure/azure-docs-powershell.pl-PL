---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenanceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenanceConfiguration.md
ms.openlocfilehash: d7bfd36c54d1a141a41d23ede168a64752e1fcd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220617"
---
# <span data-ttu-id="c5d82-101">Get-AzMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5d82-101">Get-AzMaintenanceConfiguration</span></span>

## <span data-ttu-id="c5d82-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5d82-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d82-103">Pobierz rekord konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="c5d82-103">Get Maintenance configuration record</span></span>

## <span data-ttu-id="c5d82-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5d82-104">SYNTAX</span></span>

```
Get-AzMaintenanceConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5d82-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c5d82-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d82-106">Pobierz rekord konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="c5d82-106">Get Maintenance configuration record</span></span>

## <span data-ttu-id="c5d82-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5d82-107">EXAMPLES</span></span>

### <span data-ttu-id="c5d82-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5d82-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenanceConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {}
MaintenanceScope    : Host
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/maintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/maintenanceConfigurations
```

<span data-ttu-id="c5d82-109">Pobierz rekord konfiguracji konserwacji</span><span class="sxs-lookup"><span data-stu-id="c5d82-109">Get Maintenance configuration record</span></span>

## <span data-ttu-id="c5d82-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5d82-110">PARAMETERS</span></span>

### <span data-ttu-id="c5d82-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d82-111">-DefaultProfile</span></span>
<span data-ttu-id="c5d82-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5d82-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5d82-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5d82-113">-Name</span></span>
<span data-ttu-id="c5d82-114">Nazwa konfiguracji konserwacji.</span><span class="sxs-lookup"><span data-stu-id="c5d82-114">The maintenance configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d82-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d82-115">-ResourceGroupName</span></span>
<span data-ttu-id="c5d82-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c5d82-116">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5d82-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d82-117">CommonParameters</span></span>
<span data-ttu-id="c5d82-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5d82-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d82-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5d82-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d82-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5d82-120">INPUTS</span></span>

### <span data-ttu-id="c5d82-121">System. String</span><span class="sxs-lookup"><span data-stu-id="c5d82-121">System.String</span></span>

## <span data-ttu-id="c5d82-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5d82-122">OUTPUTS</span></span>

### <span data-ttu-id="c5d82-123">Microsoft. Azure. Commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5d82-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="c5d82-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5d82-124">NOTES</span></span>

## <span data-ttu-id="c5d82-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5d82-125">RELATED LINKS</span></span>
