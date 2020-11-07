---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactoryGatewayAuthKey.md
ms.openlocfilehash: b7f435090c0ff5c421df7d8d3e885f67456f9af0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718616"
---
# <span data-ttu-id="c9427-101">New-AzureRmDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="c9427-101">New-AzureRmDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="c9427-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c9427-102">SYNOPSIS</span></span>
<span data-ttu-id="c9427-103">Tworzy klucz uwierzytelniania dla bramy usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c9427-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9427-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c9427-104">SYNTAX</span></span>

### <span data-ttu-id="c9427-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c9427-105">ByFactoryName (Default)</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9427-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c9427-106">ByFactoryObject</span></span>
```
New-AzureRmDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9427-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c9427-107">DESCRIPTION</span></span>
<span data-ttu-id="c9427-108">Polecenie cmdlet **New-AzureRmDataFactoryGatewayAuthKey** służy do tworzenia klucza uwierzytelniania bramy dla określonej bramy usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="c9427-108">The **New-AzureRmDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="c9427-109">Użytkownik rejestruje bramę w usłudze chmury za pomocą tego klucza.</span><span class="sxs-lookup"><span data-stu-id="c9427-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="c9427-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c9427-110">EXAMPLES</span></span>

### <span data-ttu-id="c9427-111">Przykład 1: tworzy klucz uwierzytelniania bramy dla KEY1</span><span class="sxs-lookup"><span data-stu-id="c9427-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzureRmDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="c9427-112">To polecenie tworzy klucz uwierzytelniania bramy KEY1 dla bramy fabryki danych o nazwie Moja brama.</span><span class="sxs-lookup"><span data-stu-id="c9427-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="c9427-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c9427-113">PARAMETERS</span></span>

### <span data-ttu-id="c9427-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c9427-114">-DataFactoryName</span></span>
<span data-ttu-id="c9427-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="c9427-115">The data factory name.</span></span>

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

### <span data-ttu-id="c9427-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9427-116">-DefaultProfile</span></span>
<span data-ttu-id="c9427-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c9427-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c9427-118">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="c9427-118">-GatewayName</span></span>
<span data-ttu-id="c9427-119">Nazwa bramy fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="c9427-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="c9427-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c9427-120">-InputObject</span></span>
<span data-ttu-id="c9427-121">Obiekt fabryki danych</span><span class="sxs-lookup"><span data-stu-id="c9427-121">The data factory object</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: DataFactory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c9427-122">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="c9427-122">-KeyName</span></span>
<span data-ttu-id="c9427-123">Nazwa klucza uwierzytelniania bramy do ponownego wygenerowania ("KEY1" lub "key2").</span><span class="sxs-lookup"><span data-stu-id="c9427-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9427-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9427-124">-ResourceGroupName</span></span>
<span data-ttu-id="c9427-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c9427-125">The resource group name.</span></span>

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

### <span data-ttu-id="c9427-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c9427-126">-Confirm</span></span>
<span data-ttu-id="c9427-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9427-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9427-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9427-128">-WhatIf</span></span>
<span data-ttu-id="c9427-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9427-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c9427-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c9427-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9427-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9427-131">CommonParameters</span></span>
<span data-ttu-id="c9427-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9427-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9427-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9427-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9427-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c9427-134">INPUTS</span></span>

### <span data-ttu-id="c9427-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c9427-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>
<span data-ttu-id="c9427-136">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c9427-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c9427-137">System. String</span><span class="sxs-lookup"><span data-stu-id="c9427-137">System.String</span></span>

## <span data-ttu-id="c9427-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c9427-138">OUTPUTS</span></span>

### <span data-ttu-id="c9427-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="c9427-139">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="c9427-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c9427-140">NOTES</span></span>
* <span data-ttu-id="c9427-141">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="c9427-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c9427-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c9427-142">RELATED LINKS</span></span>

<span data-ttu-id="c9427-143">[Nowe — AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md) 
 [Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="c9427-143">[New-AzureRmDataFactoryGateway](./New-AzureRmDataFactoryGateway.md)
[Get-AzureRmDataFactoryGatewayAuthKey](./Get-AzureRmDataFactoryGatewayAuthKey.md)</span></span>

