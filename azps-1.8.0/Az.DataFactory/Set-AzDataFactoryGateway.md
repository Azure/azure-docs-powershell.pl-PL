---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: 765fbe54a43ee28e2ccce8254a6f146c734b0e03
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710086"
---
# <span data-ttu-id="0625a-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0625a-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="0625a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0625a-102">SYNOPSIS</span></span>
<span data-ttu-id="0625a-103">Ustawia opis bramy w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0625a-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="0625a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0625a-104">SYNTAX</span></span>

### <span data-ttu-id="0625a-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0625a-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0625a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0625a-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0625a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0625a-107">DESCRIPTION</span></span>
<span data-ttu-id="0625a-108">Polecenie cmdlet **Set-AzDataFactoryGateway** ustawia opis określonej bramy w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0625a-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="0625a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0625a-109">EXAMPLES</span></span>

### <span data-ttu-id="0625a-110">Przykład 1: Ustawianie opisu dla bramy</span><span class="sxs-lookup"><span data-stu-id="0625a-110">Example 1: Set the description for a gateway</span></span>
```
PS C:\>Set-AzDataFactoryGateway -ResourceGroupName "ADF" -Name "ContosoGateway" -DataFactoryName "WikiADF" -Description "my gateway"
Name            : ContosoGateway
Description     : my gateway
Version         : 1.3.5338.1
Status          : Online
VersionStatus   : UpToDate
CreateTime      : 8/22/2014 1:31:09 AM
RegisterTime    : 8/22/2014 1:31:37 AM
LastConnectTime : 8/22/2014 1:41:41 AM
ExpiryTime      :
```

<span data-ttu-id="0625a-111">To polecenie ustawia opis bramy o nazwie ContosoGateway w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0625a-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="0625a-112">Parametr Description określa nowy opis.</span><span class="sxs-lookup"><span data-stu-id="0625a-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="0625a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0625a-113">PARAMETERS</span></span>

### <span data-ttu-id="0625a-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0625a-114">-DataFactory</span></span>
<span data-ttu-id="0625a-115">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="0625a-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0625a-116">To polecenie cmdlet ustawia opis bramy w fabryce danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0625a-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0625a-117">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0625a-117">-DataFactoryName</span></span>
<span data-ttu-id="0625a-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0625a-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0625a-119">To polecenie cmdlet ustawia opis bramy w fabryce danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0625a-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0625a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0625a-120">-DefaultProfile</span></span>
<span data-ttu-id="0625a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0625a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0625a-122">— Opis</span><span class="sxs-lookup"><span data-stu-id="0625a-122">-Description</span></span>
<span data-ttu-id="0625a-123">Określa opis bramy.</span><span class="sxs-lookup"><span data-stu-id="0625a-123">Specifies a description for the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0625a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0625a-124">-Name</span></span>
<span data-ttu-id="0625a-125">Określa nazwę bramy, dla której ma zostać ustawiony opis.</span><span class="sxs-lookup"><span data-stu-id="0625a-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="0625a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0625a-126">-ResourceGroupName</span></span>
<span data-ttu-id="0625a-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0625a-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0625a-128">To polecenie cmdlet ustawia opis bramy należącej do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="0625a-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0625a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0625a-129">CommonParameters</span></span>
<span data-ttu-id="0625a-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0625a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0625a-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0625a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0625a-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0625a-132">INPUTS</span></span>

### <span data-ttu-id="0625a-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0625a-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="0625a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0625a-134">System.String</span></span>

## <span data-ttu-id="0625a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0625a-135">OUTPUTS</span></span>

### <span data-ttu-id="0625a-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0625a-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="0625a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0625a-137">NOTES</span></span>
* <span data-ttu-id="0625a-138">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="0625a-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0625a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0625a-139">RELATED LINKS</span></span>

[<span data-ttu-id="0625a-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0625a-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="0625a-141">Nowe — AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0625a-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="0625a-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="0625a-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


