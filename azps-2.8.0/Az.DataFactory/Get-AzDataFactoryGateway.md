---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryGateway.md
ms.openlocfilehash: da5ae19a03b34a04fc9928d684910e759303cedd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706050"
---
# <span data-ttu-id="184dc-101">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="184dc-101">Get-AzDataFactoryGateway</span></span>

## <span data-ttu-id="184dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="184dc-102">SYNOPSIS</span></span>
<span data-ttu-id="184dc-103">Pobiera informacje o bramach logicznych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="184dc-103">Gets information about logical gateways in Azure Data Factory.</span></span>

## <span data-ttu-id="184dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="184dc-104">SYNTAX</span></span>

### <span data-ttu-id="184dc-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="184dc-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="184dc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="184dc-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="184dc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="184dc-107">DESCRIPTION</span></span>
<span data-ttu-id="184dc-108">Polecenie cmdlet **Get-AzDataFactoryGateway** pobiera informacje o logicznych bramach usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="184dc-108">The **Get-AzDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="184dc-109">Jeśli określisz nazwę bramy, to polecenie cmdlet będzie pobierać informacje o tej bramie.</span><span class="sxs-lookup"><span data-stu-id="184dc-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="184dc-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich bram dla fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="184dc-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>
<span data-ttu-id="184dc-111">Jeśli chcesz dodać lokalny program Microsoft SQL Server jako połączoną usługę do fabryki danych, musisz zainstalować bramę na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="184dc-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="184dc-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="184dc-112">EXAMPLES</span></span>

### <span data-ttu-id="184dc-113">Przykład 1: uzyskiwanie wszystkich bram logicznych w fabryce danych</span><span class="sxs-lookup"><span data-stu-id="184dc-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
Name            : gateway1
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      : 
Name            : gateway2
Description     : 
Version         : 1.3.5338.1
Status          : Offline
VersionStatus   : UpToDate
CreateTime      : 8/29/2014 1:46:44 AM
RegisterTime    : 8/29/2014 1:48:36 AM
LastConnectTime : 8/29/2014 1:56:56 AM
ExpiryTime      :
```

<span data-ttu-id="184dc-114">To polecenie pobiera informacje dotyczące wszystkich bram logicznych dla fabryki danych o nazwie WikiADF w grupie zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="184dc-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="184dc-115">Przykład 2: uzyskiwanie określonej bramy logicznej w fabryce danych</span><span class="sxs-lookup"><span data-stu-id="184dc-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
Name            : Gateway01
Description     : 
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:40:34 AM
RegisterTime    : 8/22/2014 1:41:46 AM
LastConnectTime : 8/22/2014 1:44:56 AM
ExpiryTime      :
```

<span data-ttu-id="184dc-116">To polecenie pobiera informacje o bramie logicznym o nazwie Gateway01 w fabryce danych o nazwie WikiADF w grupie zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="184dc-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="184dc-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="184dc-117">PARAMETERS</span></span>

### <span data-ttu-id="184dc-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="184dc-118">-DataFactory</span></span>
<span data-ttu-id="184dc-119">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="184dc-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="184dc-120">To polecenie cmdlet umożliwia pobieranie informacji o bramach logicznych w fabryce danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="184dc-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184dc-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="184dc-121">-DataFactoryName</span></span>
<span data-ttu-id="184dc-122">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="184dc-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="184dc-123">To polecenie cmdlet umożliwia pobieranie informacji o bramach logicznych w fabryce danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="184dc-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184dc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="184dc-124">-DefaultProfile</span></span>
<span data-ttu-id="184dc-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="184dc-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="184dc-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="184dc-126">-Name</span></span>
<span data-ttu-id="184dc-127">Określa nazwę bramy logicznej, o której należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="184dc-127">Specifies the name of the logical gateway about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184dc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="184dc-128">-ResourceGroupName</span></span>
<span data-ttu-id="184dc-129">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="184dc-129">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="184dc-130">To polecenie cmdlet umożliwia pobieranie informacji o logicznych bramach należących do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="184dc-130">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="184dc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="184dc-131">CommonParameters</span></span>
<span data-ttu-id="184dc-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="184dc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="184dc-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="184dc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="184dc-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="184dc-134">INPUTS</span></span>

### <span data-ttu-id="184dc-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="184dc-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="184dc-136">System. String</span><span class="sxs-lookup"><span data-stu-id="184dc-136">System.String</span></span>

## <span data-ttu-id="184dc-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="184dc-137">OUTPUTS</span></span>

### <span data-ttu-id="184dc-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="184dc-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="184dc-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="184dc-139">NOTES</span></span>
* <span data-ttu-id="184dc-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="184dc-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="184dc-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="184dc-141">RELATED LINKS</span></span>

[<span data-ttu-id="184dc-142">Nowe — AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="184dc-142">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="184dc-143">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="184dc-143">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)

[<span data-ttu-id="184dc-144">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="184dc-144">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)

