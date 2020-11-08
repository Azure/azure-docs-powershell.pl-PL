---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusMigration.md
ms.openlocfilehash: 686a2486d6a5e28e0149eb8fbf2387744d545fd0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052717"
---
# <span data-ttu-id="03336-101">Get-AzServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="03336-101">Get-AzServiceBusMigration</span></span>

## <span data-ttu-id="03336-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03336-102">SYNOPSIS</span></span>
<span data-ttu-id="03336-103">Pobiera MigrationConfiguration dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="03336-103">Retrieves MigrationConfiguration for the namespace</span></span>

## <span data-ttu-id="03336-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03336-104">SYNTAX</span></span>

### <span data-ttu-id="03336-105">MigrationConfigurationPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03336-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03336-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="03336-106">NamespaceInputObjectSet</span></span>
```
Get-AzServiceBusMigration [-InputObject] <PSNamespaceAttributes> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03336-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03336-107">ResourceIdParameterSet</span></span>
```
Get-AzServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03336-108">Opis</span><span class="sxs-lookup"><span data-stu-id="03336-108">DESCRIPTION</span></span>
<span data-ttu-id="03336-109">**AzServiceBusMigration** Pobiera konfigurację migracji dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="03336-109">The **Get-AzServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="03336-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03336-110">EXAMPLES</span></span>

### <span data-ttu-id="03336-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="03336-111">Example 1</span></span>
```powershell
PS C:\> Get-AzServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMigration

Name              : TestingNamespaceStandardMigration
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMigration/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMigration
PostMigrationName : TestingNamespaceStandardMigrationPostMigration
```

<span data-ttu-id="03336-112">Pobiera właściwości konfiguracji migracji z "TestingNamespaceStandardMigration"</span><span class="sxs-lookup"><span data-stu-id="03336-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMigration'</span></span>

## <span data-ttu-id="03336-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03336-113">PARAMETERS</span></span>

### <span data-ttu-id="03336-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03336-114">-DefaultProfile</span></span>
<span data-ttu-id="03336-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03336-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03336-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="03336-116">-InputObject</span></span>
<span data-ttu-id="03336-117">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="03336-117">Namespace Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes
Parameter Sets: NamespaceInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03336-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03336-118">-Name</span></span>
<span data-ttu-id="03336-119">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="03336-119">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03336-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03336-120">-ResourceGroupName</span></span>
<span data-ttu-id="03336-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="03336-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: MigrationConfigurationPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03336-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03336-122">-ResourceId</span></span>
<span data-ttu-id="03336-123">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="03336-123">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03336-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03336-124">CommonParameters</span></span>
<span data-ttu-id="03336-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03336-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03336-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03336-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03336-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03336-127">INPUTS</span></span>

### <span data-ttu-id="03336-128">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="03336-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

### <span data-ttu-id="03336-129">System. String</span><span class="sxs-lookup"><span data-stu-id="03336-129">System.String</span></span>

## <span data-ttu-id="03336-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03336-130">OUTPUTS</span></span>

### <span data-ttu-id="03336-131">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="03336-131">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="03336-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03336-132">NOTES</span></span>

## <span data-ttu-id="03336-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03336-133">RELATED LINKS</span></span>
