---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusmigration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusMigration.md
ms.openlocfilehash: cdf869f13c90982c40568f37c0757ef2e7547b3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546488"
---
# <span data-ttu-id="77c71-101">Get-AzureRmServiceBusMigration</span><span class="sxs-lookup"><span data-stu-id="77c71-101">Get-AzureRmServiceBusMigration</span></span>

## <span data-ttu-id="77c71-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77c71-102">SYNOPSIS</span></span>
<span data-ttu-id="77c71-103">Pobiera MigrationConfiguration dla obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="77c71-103">Retrieves MigrationConfiguration for the namespace</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77c71-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77c71-104">SYNTAX</span></span>

### <span data-ttu-id="77c71-105">MigrationConfigurationPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77c71-105">MigrationConfigurationPropertiesSet (Default)</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77c71-106">NamespaceInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="77c71-106">NamespaceInputObjectSet</span></span>
```
Get-AzureRmServiceBusMigration [-InputObject] <PSNamespaceAttributes>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77c71-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77c71-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmServiceBusMigration [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77c71-108">Opis</span><span class="sxs-lookup"><span data-stu-id="77c71-108">DESCRIPTION</span></span>
<span data-ttu-id="77c71-109">**AzureRmServiceBusMigration** Pobiera konfigurację migracji dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="77c71-109">The **Get-AzureRmServiceBusMigration** Retrieves Migration Configuration for the namespace</span></span>

## <span data-ttu-id="77c71-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77c71-110">EXAMPLES</span></span>

### <span data-ttu-id="77c71-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77c71-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmServiceBusMigration -ResourceGroupName ResourceGroup -Name TestingNamespaceStandardMirgation

Name              : TestingNamespaceStandardMirgation
Id                : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespaceStandardMirgation/migrationConfigurations/$default
Type              : Microsoft.ServiceBus/Namespaces/migrationconfigurations
ProvisioningState : Succeeded
PendingReplicationOperationsCount : 40
TargetNamespace   : /subscriptions/d7670b40-0217-4af9-985c-972f6702782e/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/TestingNamespacePremiumMirgation
PostMigrationName : TestingNamespaceStandardMirgationPostMigration
```

<span data-ttu-id="77c71-112">Pobiera właściwości konfiguracji migracji z "TestingNamespaceStandardMirgation"</span><span class="sxs-lookup"><span data-stu-id="77c71-112">Gets the Migration Configuration properties of 'TestingNamespaceStandardMirgation'</span></span>

## <span data-ttu-id="77c71-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77c71-113">PARAMETERS</span></span>

### <span data-ttu-id="77c71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77c71-114">-DefaultProfile</span></span>
<span data-ttu-id="77c71-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77c71-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77c71-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77c71-116">-InputObject</span></span>
<span data-ttu-id="77c71-117">Obiekt Namespace</span><span class="sxs-lookup"><span data-stu-id="77c71-117">Namespace Object</span></span>

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

### <span data-ttu-id="77c71-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="77c71-118">-Name</span></span>
<span data-ttu-id="77c71-119">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="77c71-119">Namespace Name</span></span>

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

### <span data-ttu-id="77c71-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77c71-120">-ResourceGroupName</span></span>
<span data-ttu-id="77c71-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="77c71-121">Resource Group Name</span></span>

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

### <span data-ttu-id="77c71-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77c71-122">-ResourceId</span></span>
<span data-ttu-id="77c71-123">Identyfikator zasobu obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="77c71-123">Namespace Resource Id</span></span>

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

### <span data-ttu-id="77c71-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77c71-124">CommonParameters</span></span>
<span data-ttu-id="77c71-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77c71-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77c71-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77c71-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77c71-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77c71-127">INPUTS</span></span>

### <span data-ttu-id="77c71-128">Microsoft. Azure. Commands. ServiceBus. models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="77c71-128">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>
<span data-ttu-id="77c71-129">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="77c71-129">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="77c71-130">System. String</span><span class="sxs-lookup"><span data-stu-id="77c71-130">System.String</span></span>

## <span data-ttu-id="77c71-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77c71-131">OUTPUTS</span></span>

### <span data-ttu-id="77c71-132">Microsoft. Azure. Commands. ServiceBus. models. PSServiceBusMigrationConfigurationAttributes</span><span class="sxs-lookup"><span data-stu-id="77c71-132">Microsoft.Azure.Commands.ServiceBus.Models.PSServiceBusMigrationConfigurationAttributes</span></span>

## <span data-ttu-id="77c71-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77c71-133">NOTES</span></span>

## <span data-ttu-id="77c71-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77c71-134">RELATED LINKS</span></span>
