---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: D85FF5ED-23EA-48C7-8E61-D931713E0064
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryGateway.md
ms.openlocfilehash: a90146480b0706d88f4ef7626b83008e08c22232
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719354"
---
# <span data-ttu-id="f5f91-101">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f5f91-101">Get-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="f5f91-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5f91-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f91-103">Pobiera informacje o bramach logicznych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f5f91-103">Gets information about logical gateways in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5f91-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5f91-104">SYNTAX</span></span>

### <span data-ttu-id="f5f91-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f5f91-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactoryName] <String> [[-Name] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f5f91-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f5f91-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5f91-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f5f91-107">DESCRIPTION</span></span>
<span data-ttu-id="f5f91-108">Polecenie cmdlet **Get-AzureRmDataFactoryGateway** pobiera informacje o logicznych bramach usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f5f91-108">The **Get-AzureRmDataFactoryGateway** cmdlet gets information about logical gateways in Azure Data Factory.</span></span>
<span data-ttu-id="f5f91-109">Jeśli określisz nazwę bramy, to polecenie cmdlet będzie pobierać informacje o tej bramie.</span><span class="sxs-lookup"><span data-stu-id="f5f91-109">If you specify the name of a gateway, this cmdlet gets information about that gateway.</span></span>
<span data-ttu-id="f5f91-110">Jeśli nie określisz nazwy, to polecenie cmdlet będzie pobierać informacje dotyczące wszystkich bram dla fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="f5f91-110">If you do not specify a name, this cmdlet gets information about all gateways for a data factory.</span></span>

<span data-ttu-id="f5f91-111">Jeśli chcesz dodać lokalny program Microsoft SQL Server jako połączoną usługę do fabryki danych, musisz zainstalować bramę na komputerze lokalnym.</span><span class="sxs-lookup"><span data-stu-id="f5f91-111">If you want to add an on-premises Microsoft SQL Server as a linked service to a data factory, you must install a gateway on your on-premises computer.</span></span>

## <span data-ttu-id="f5f91-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5f91-112">EXAMPLES</span></span>

### <span data-ttu-id="f5f91-113">Przykład 1: uzyskiwanie wszystkich bram logicznych w fabryce danych</span><span class="sxs-lookup"><span data-stu-id="f5f91-113">Example 1: Get all logical gateways in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -DataFactoryName "WikiADF"
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

<span data-ttu-id="f5f91-114">To polecenie pobiera informacje dotyczące wszystkich bram logicznych dla fabryki danych o nazwie WikiADF w grupie zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="f5f91-114">This command gets information about all logical gateways for the data factory named WikiADF in the resource group named ADF.</span></span>

### <span data-ttu-id="f5f91-115">Przykład 2: uzyskiwanie określonej bramy logicznej w fabryce danych</span><span class="sxs-lookup"><span data-stu-id="f5f91-115">Example 2: Get a specific logical gateway in a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryGateway -ResourceGroupName "ADF" -Name "Gateway01" -DataFactoryName "WikiADF"
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

<span data-ttu-id="f5f91-116">To polecenie pobiera informacje o bramie logicznym o nazwie Gateway01 w fabryce danych o nazwie WikiADF w grupie zasobów o nazwie ADF.</span><span class="sxs-lookup"><span data-stu-id="f5f91-116">This command gets information about the logical gateway named Gateway01 in the data factory named WikiADF in the resource group named ADF.</span></span>

## <span data-ttu-id="f5f91-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5f91-117">PARAMETERS</span></span>

### <span data-ttu-id="f5f91-118">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f5f91-118">-DataFactory</span></span>
<span data-ttu-id="f5f91-119">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="f5f91-119">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f5f91-120">To polecenie cmdlet umożliwia pobieranie informacji o bramach logicznych w fabryce danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f5f91-120">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5f91-121">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f5f91-121">-DataFactoryName</span></span>
<span data-ttu-id="f5f91-122">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="f5f91-122">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f5f91-123">To polecenie cmdlet umożliwia pobieranie informacji o bramach logicznych w fabryce danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f5f91-123">This cmdlet gets information about logical gateways in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5f91-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f5f91-124">-Name</span></span>
<span data-ttu-id="f5f91-125">Określa nazwę bramy logicznej, o której należy uzyskać informacje.</span><span class="sxs-lookup"><span data-stu-id="f5f91-125">Specifies the name of the logical gateway about which to get information.</span></span>

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

### <span data-ttu-id="f5f91-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f91-126">-ResourceGroupName</span></span>
<span data-ttu-id="f5f91-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f91-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f5f91-128">To polecenie cmdlet umożliwia pobieranie informacji o logicznych bramach należących do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="f5f91-128">This cmdlet gets information about logical gateways that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f5f91-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f91-129">-DefaultProfile</span></span>
<span data-ttu-id="f5f91-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5f91-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5f91-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f91-131">CommonParameters</span></span>
<span data-ttu-id="f5f91-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f91-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f91-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f91-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f91-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5f91-134">INPUTS</span></span>

## <span data-ttu-id="f5f91-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5f91-135">OUTPUTS</span></span>

### <span data-ttu-id="f5f91-136">System. Collections. Generic. list "1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f5f91-136">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway]], Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryGateway</span></span>

## <span data-ttu-id="f5f91-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5f91-137">NOTES</span></span>
* <span data-ttu-id="f5f91-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="f5f91-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f5f91-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5f91-139">RELATED LINKS</span></span>

[<span data-ttu-id="f5f91-140">Nowe — AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f5f91-140">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="f5f91-141">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f5f91-141">Remove-AzureRmDataFactoryGateway</span></span>](./Remove-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="f5f91-142">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f5f91-142">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


