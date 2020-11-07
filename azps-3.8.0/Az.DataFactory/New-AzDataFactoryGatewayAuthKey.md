---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: 541cedecbad563be3e1a016dd651d3e93af44d1e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896389"
---
# <span data-ttu-id="0a57f-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="0a57f-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="0a57f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a57f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a57f-103">Tworzy klucz uwierzytelniania dla bramy usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0a57f-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="0a57f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a57f-104">SYNTAX</span></span>

### <span data-ttu-id="0a57f-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0a57f-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0a57f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0a57f-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a57f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0a57f-107">DESCRIPTION</span></span>
<span data-ttu-id="0a57f-108">Polecenie cmdlet **New-AzDataFactoryGatewayAuthKey** służy do tworzenia klucza uwierzytelniania bramy dla określonej bramy usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0a57f-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="0a57f-109">Użytkownik rejestruje bramę w usłudze chmury za pomocą tego klucza.</span><span class="sxs-lookup"><span data-stu-id="0a57f-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="0a57f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a57f-110">EXAMPLES</span></span>

### <span data-ttu-id="0a57f-111">Przykład 1: tworzy klucz uwierzytelniania bramy dla KEY1</span><span class="sxs-lookup"><span data-stu-id="0a57f-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="0a57f-112">To polecenie tworzy klucz uwierzytelniania bramy KEY1 dla bramy fabryki danych o nazwie Moja brama.</span><span class="sxs-lookup"><span data-stu-id="0a57f-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="0a57f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a57f-113">PARAMETERS</span></span>

### <span data-ttu-id="0a57f-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0a57f-114">-DataFactoryName</span></span>
<span data-ttu-id="0a57f-115">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0a57f-115">The data factory name.</span></span>

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

### <span data-ttu-id="0a57f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a57f-116">-DefaultProfile</span></span>
<span data-ttu-id="0a57f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0a57f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a57f-118">-Bramaname</span><span class="sxs-lookup"><span data-stu-id="0a57f-118">-GatewayName</span></span>
<span data-ttu-id="0a57f-119">Nazwa bramy fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0a57f-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="0a57f-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0a57f-120">-InputObject</span></span>
<span data-ttu-id="0a57f-121">Obiekt fabryki danych</span><span class="sxs-lookup"><span data-stu-id="0a57f-121">The data factory object</span></span>

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

### <span data-ttu-id="0a57f-122">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="0a57f-122">-KeyName</span></span>
<span data-ttu-id="0a57f-123">Nazwa klucza uwierzytelniania bramy do ponownego wygenerowania ("KEY1" lub "key2").</span><span class="sxs-lookup"><span data-stu-id="0a57f-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

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

### <span data-ttu-id="0a57f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a57f-124">-ResourceGroupName</span></span>
<span data-ttu-id="0a57f-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0a57f-125">The resource group name.</span></span>

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

### <span data-ttu-id="0a57f-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0a57f-126">-Confirm</span></span>
<span data-ttu-id="0a57f-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a57f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a57f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a57f-128">-WhatIf</span></span>
<span data-ttu-id="0a57f-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a57f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a57f-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0a57f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a57f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a57f-131">CommonParameters</span></span>
<span data-ttu-id="0a57f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a57f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a57f-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a57f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a57f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a57f-134">INPUTS</span></span>

### <span data-ttu-id="0a57f-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0a57f-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="0a57f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0a57f-136">System.String</span></span>

## <span data-ttu-id="0a57f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a57f-137">OUTPUTS</span></span>

### <span data-ttu-id="0a57f-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="0a57f-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="0a57f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a57f-139">NOTES</span></span>
* <span data-ttu-id="0a57f-140">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="0a57f-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0a57f-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a57f-141">RELATED LINKS</span></span>

<span data-ttu-id="0a57f-142">[Nowe — AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="0a57f-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

