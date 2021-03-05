---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/new-azdatafactorygatewayauthkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactoryGatewayAuthKey.md
ms.openlocfilehash: e58df40aa227e1c8132902c467c2dbcb881c7b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974961"
---
# <span data-ttu-id="efc29-101">New-AzDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="efc29-101">New-AzDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="efc29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efc29-102">SYNOPSIS</span></span>
<span data-ttu-id="efc29-103">Tworzy klucz uwierzytelniania dla bramy Azure Data Factory Gateway.</span><span class="sxs-lookup"><span data-stu-id="efc29-103">Creates auth key for an Azure Data Factory Gateway.</span></span>

## <span data-ttu-id="efc29-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="efc29-104">SYNTAX</span></span>

### <span data-ttu-id="efc29-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="efc29-105">ByFactoryName (Default)</span></span>
```
New-AzDataFactoryGatewayAuthKey [-DataFactoryName] <String> [-GatewayName] <String> [-KeyName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efc29-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="efc29-106">ByFactoryObject</span></span>
```
New-AzDataFactoryGatewayAuthKey [-InputObject] <PSDataFactory> [-GatewayName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="efc29-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="efc29-107">DESCRIPTION</span></span>
<span data-ttu-id="efc29-108">Polecenie **cmdlet New-AzDataFactoryGatewayAuthKey** tworzy klucz uwierzytelniania bramy dla określonej bramy usługi Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="efc29-108">The **New-AzDataFactoryGatewayAuthKey** cmdlet creates gateway auth key for a specified Azure Data Factory gateway.</span></span>
<span data-ttu-id="efc29-109">Za pomocą tego klucza zarejestrujesz bramę w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="efc29-109">You register the gateway with a cloud service by using this key.</span></span>

## <span data-ttu-id="efc29-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="efc29-110">EXAMPLES</span></span>

### <span data-ttu-id="efc29-111">Przykład 1. Tworzy klucz uwierzytelniania bramy dla klucza 1</span><span class="sxs-lookup"><span data-stu-id="efc29-111">Example 1: Creates a gateway auth key for Key1</span></span>
```
PS C:\> New-AzDataFactoryGatewayAuthKey -ResourceGroup ADFResource -GatewayName 'MyGateway' -DataFactoryName MyADF -KeyName key1
Key1 : DMG@632e739e-1053-4070-9102-8591f067526e@41fcbc45-c594-4152-a8f1-fcbcd6452aea@wu@BH0EV9hu/o2IYGQzfYYD203XhdS6Tty
       fkYwYFbG6wBU=
Key2 :
```

<span data-ttu-id="efc29-112">To polecenie tworzy klucz uwierzytelniania bramy klucz1 dla bramy fabrycznej danych o nazwie MyGateway.</span><span class="sxs-lookup"><span data-stu-id="efc29-112">This command creates a gateway auth key of Key1 for the data factory gateway named MyGateway.</span></span>

## <span data-ttu-id="efc29-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efc29-113">PARAMETERS</span></span>

### <span data-ttu-id="efc29-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="efc29-114">-DataFactoryName</span></span>
<span data-ttu-id="efc29-115">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="efc29-115">The data factory name.</span></span>

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

### <span data-ttu-id="efc29-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc29-116">-DefaultProfile</span></span>
<span data-ttu-id="efc29-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="efc29-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="efc29-118">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="efc29-118">-GatewayName</span></span>
<span data-ttu-id="efc29-119">Nazwa bramy fabrycznej danych.</span><span class="sxs-lookup"><span data-stu-id="efc29-119">The data factory gateway name.</span></span>

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

### <span data-ttu-id="efc29-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="efc29-120">-InputObject</span></span>
<span data-ttu-id="efc29-121">Obiekt data factory</span><span class="sxs-lookup"><span data-stu-id="efc29-121">The data factory object</span></span>

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

### <span data-ttu-id="efc29-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="efc29-122">-KeyName</span></span>
<span data-ttu-id="efc29-123">Nazwa klucza uwierzytelniania bramy do ponownego wygenerowania: "klucz1" lub "klucz2".</span><span class="sxs-lookup"><span data-stu-id="efc29-123">The name of gateway auth key to be regenerated, either 'key1' or 'key2'.</span></span>

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

### <span data-ttu-id="efc29-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc29-124">-ResourceGroupName</span></span>
<span data-ttu-id="efc29-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="efc29-125">The resource group name.</span></span>

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

### <span data-ttu-id="efc29-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="efc29-126">-Confirm</span></span>
<span data-ttu-id="efc29-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="efc29-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efc29-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efc29-128">-WhatIf</span></span>
<span data-ttu-id="efc29-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efc29-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efc29-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="efc29-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efc29-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc29-131">CommonParameters</span></span>
<span data-ttu-id="efc29-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc29-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc29-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc29-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc29-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efc29-134">INPUTS</span></span>

### <span data-ttu-id="efc29-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="efc29-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="efc29-136">System.String</span><span class="sxs-lookup"><span data-stu-id="efc29-136">System.String</span></span>

## <span data-ttu-id="efc29-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efc29-137">OUTPUTS</span></span>

### <span data-ttu-id="efc29-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span><span class="sxs-lookup"><span data-stu-id="efc29-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactoryGatewayAuthKey</span></span>

## <span data-ttu-id="efc29-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="efc29-139">NOTES</span></span>
* <span data-ttu-id="efc29-140">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="efc29-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="efc29-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efc29-141">RELATED LINKS</span></span>

<span data-ttu-id="efc29-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md) 
 [Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span><span class="sxs-lookup"><span data-stu-id="efc29-142">[New-AzDataFactoryGateway](./New-AzDataFactoryGateway.md)
[Get-AzDataFactoryGatewayAuthKey](./Get-AzDataFactoryGatewayAuthKey.md)</span></span>

