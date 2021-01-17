---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/en-us/powershell/module/az.maintenance/get-azmaintenancepublicconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Get-AzMaintenancePublicConfiguration.md
ms.openlocfilehash: 8df9e8145e1acb03c0351f30565da2d9a8ed4a9d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385814"
---
# <span data-ttu-id="233e3-101">Get-AzMaintenancePublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="233e3-101">Get-AzMaintenancePublicConfiguration</span></span>

## <span data-ttu-id="233e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="233e3-102">SYNOPSIS</span></span>
<span data-ttu-id="233e3-103">Pobieranie rekordu konfiguracji konserwacji publicznej</span><span class="sxs-lookup"><span data-stu-id="233e3-103">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="233e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="233e3-104">SYNTAX</span></span>

```
Get-AzMaintenancePublicConfiguration [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="233e3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="233e3-105">DESCRIPTION</span></span>
<span data-ttu-id="233e3-106">Pobieranie rekordu konfiguracji konserwacji publicznej</span><span class="sxs-lookup"><span data-stu-id="233e3-106">Get Public Maintenance Configuration record</span></span>

## <span data-ttu-id="233e3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="233e3-107">EXAMPLES</span></span>

### <span data-ttu-id="233e3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="233e3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzMaintenancePublicConfiguration -ResourceGroupName smdtest -Name workervmscentralus


Location            : centralus
Tags                : {}
NamespaceProperty   :
ExtensionProperties : {"publicMaintenanceConfigurationId" : "workervmscentralus"}
StartDateTime       : 2020-08-01 00:00
ExpirationDateTime  : 2021-08-04 00:00
TimeZone            : Pacific Standard Time
RecurEvery          : Day
Duration            : 05:00
MaintenanceScope    : SQLDB
Visibility          : Public
Id                  : /subscriptions/42c974dd-2c03-4f1b-96ad-b07f050aaa74/resourcegroups/smdtest/providers/Microsoft.Maintenance/publicMaintenanceConfigurations/workervmscentralus
Name                : workervmscentralus
Type                : Microsoft.Maintenance/publicMaintenanceConfigurations
```

<span data-ttu-id="233e3-109">Pobieranie rekordu konfiguracji konserwacji publicznej</span><span class="sxs-lookup"><span data-stu-id="233e3-109">Get Public Maintenance configuration record</span></span>

## <span data-ttu-id="233e3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="233e3-110">PARAMETERS</span></span>

### <span data-ttu-id="233e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="233e3-111">-DefaultProfile</span></span>
<span data-ttu-id="233e3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="233e3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="233e3-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="233e3-113">-Name</span></span>
<span data-ttu-id="233e3-114">Nazwa konfiguracji trybu konserwacji publicznej.</span><span class="sxs-lookup"><span data-stu-id="233e3-114">The public maintenance configuration Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="233e3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="233e3-115">-ResourceGroupName</span></span>
<span data-ttu-id="233e3-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="233e3-116">The resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="233e3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="233e3-117">CommonParameters</span></span>
<span data-ttu-id="233e3-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="233e3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="233e3-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="233e3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="233e3-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="233e3-120">INPUTS</span></span>

### <span data-ttu-id="233e3-121">System. String</span><span class="sxs-lookup"><span data-stu-id="233e3-121">System.String</span></span>

## <span data-ttu-id="233e3-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="233e3-122">OUTPUTS</span></span>

### <span data-ttu-id="233e3-123">Microsoft. Azure. Commands. Maintenance. models. PSMaintenanceConfiguration</span><span class="sxs-lookup"><span data-stu-id="233e3-123">Microsoft.Azure.Commands.Maintenance.Models.PSMaintenanceConfiguration</span></span>

## <span data-ttu-id="233e3-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="233e3-124">NOTES</span></span>

## <span data-ttu-id="233e3-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="233e3-125">RELATED LINKS</span></span>
