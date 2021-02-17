---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 663D27A3-0B51-48F5-81D0-8DDBC5A3A33C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryGateway.md
ms.openlocfilehash: b9eebe26e64e9a7ce2497cdf9984ca6dabb062e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177147"
---
# <span data-ttu-id="f894e-101">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f894e-101">Set-AzDataFactoryGateway</span></span>

## <span data-ttu-id="f894e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f894e-102">SYNOPSIS</span></span>
<span data-ttu-id="f894e-103">Ustawia opis bramy w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f894e-103">Sets the description for a gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="f894e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f894e-104">SYNTAX</span></span>

### <span data-ttu-id="f894e-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="f894e-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Description] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f894e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f894e-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f894e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f894e-107">DESCRIPTION</span></span>
<span data-ttu-id="f894e-108">Polecenie **cmdlet Set-AzDataFactoryGateway** ustawia opis określonej bramy w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="f894e-108">The **Set-AzDataFactoryGateway** cmdlet sets the description for the specified gateway in Azure Data Factory.</span></span>

## <span data-ttu-id="f894e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f894e-109">EXAMPLES</span></span>

### <span data-ttu-id="f894e-110">Przykład 1. Ustawianie opisu bramy</span><span class="sxs-lookup"><span data-stu-id="f894e-110">Example 1: Set the description for a gateway</span></span>
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

<span data-ttu-id="f894e-111">To polecenie ustawia opis bramy o nazwie ContosoGateway w zakładzie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="f894e-111">This command sets the description for the gateway named ContosoGateway in the data factory named WikiADF.</span></span>
<span data-ttu-id="f894e-112">Parametr Description określa nowy opis.</span><span class="sxs-lookup"><span data-stu-id="f894e-112">The Description parameter specifies the new description.</span></span>

## <span data-ttu-id="f894e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f894e-113">PARAMETERS</span></span>

### <span data-ttu-id="f894e-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f894e-114">-DataFactory</span></span>
<span data-ttu-id="f894e-115">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="f894e-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="f894e-116">To polecenie cmdlet ustawia opis bramy w zakładzie danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f894e-116">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f894e-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f894e-117">-DataFactoryName</span></span>
<span data-ttu-id="f894e-118">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="f894e-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="f894e-119">To polecenie cmdlet ustawia opis bramy w zakładzie danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f894e-119">This cmdlet sets the description for the gateway in the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="f894e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f894e-120">-DefaultProfile</span></span>
<span data-ttu-id="f894e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f894e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f894e-122">— Opis</span><span class="sxs-lookup"><span data-stu-id="f894e-122">-Description</span></span>
<span data-ttu-id="f894e-123">Określa opis bramy.</span><span class="sxs-lookup"><span data-stu-id="f894e-123">Specifies a description for the gateway.</span></span>

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

### <span data-ttu-id="f894e-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f894e-124">-Name</span></span>
<span data-ttu-id="f894e-125">Określa nazwę bramy, dla której ma być ustawiany opis.</span><span class="sxs-lookup"><span data-stu-id="f894e-125">Specifies the name of the gateway for which to set a description.</span></span>

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

### <span data-ttu-id="f894e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f894e-126">-ResourceGroupName</span></span>
<span data-ttu-id="f894e-127">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f894e-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="f894e-128">To polecenie cmdlet ustawia opis bramy należącej do grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="f894e-128">This cmdlet sets the description for a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="f894e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f894e-129">CommonParameters</span></span>
<span data-ttu-id="f894e-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f894e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f894e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f894e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f894e-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f894e-132">INPUTS</span></span>

### <span data-ttu-id="f894e-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f894e-133">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="f894e-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f894e-134">System.String</span></span>

## <span data-ttu-id="f894e-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f894e-135">OUTPUTS</span></span>

### <span data-ttu-id="f894e-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f894e-136">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGateway</span></span>

## <span data-ttu-id="f894e-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f894e-137">NOTES</span></span>
* <span data-ttu-id="f894e-138">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="f894e-138">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f894e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f894e-139">RELATED LINKS</span></span>

[<span data-ttu-id="f894e-140">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f894e-140">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="f894e-141">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f894e-141">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="f894e-142">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="f894e-142">Remove-AzDataFactoryGateway</span></span>](./Remove-AzDataFactoryGateway.md)


