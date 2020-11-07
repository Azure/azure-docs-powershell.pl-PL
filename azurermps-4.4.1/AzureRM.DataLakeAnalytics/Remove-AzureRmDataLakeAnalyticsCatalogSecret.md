---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 16716b0df5867832d51ed00797f19d5dfc0f0b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718243"
---
# <span data-ttu-id="a8ecb-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="a8ecb-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="a8ecb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8ecb-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ecb-103">Usuwa klucz tajny Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8ecb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8ecb-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8ecb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a8ecb-105">DESCRIPTION</span></span>
<span data-ttu-id="a8ecb-106">Polecenie cmdlet **Remove-AzureRmDataLakeAnalyticsCatalogSecret** usuwa hasło wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="a8ecb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8ecb-107">EXAMPLES</span></span>

### <span data-ttu-id="a8ecb-108">Przykład 1. Usuń klucz tajny</span><span class="sxs-lookup"><span data-stu-id="a8ecb-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="a8ecb-109">To polecenie usuwa określone hasło wykazu usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="a8ecb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8ecb-110">PARAMETERS</span></span>

### <span data-ttu-id="a8ecb-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="a8ecb-111">-Account</span></span>
<span data-ttu-id="a8ecb-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ecb-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a8ecb-113">-DatabaseName</span></span>
<span data-ttu-id="a8ecb-114">Określa nazwę bazy danych, która zawiera klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-114">Specifies the name of the database that holds the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8ecb-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a8ecb-115">-Force</span></span>
<span data-ttu-id="a8ecb-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ecb-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a8ecb-117">-Name</span></span>
<span data-ttu-id="a8ecb-118">Określa nazwę wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-118">Specifies the name of the secret.</span></span>

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

### <span data-ttu-id="a8ecb-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8ecb-119">-PassThru</span></span>
<span data-ttu-id="a8ecb-120">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a8ecb-121">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ecb-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8ecb-122">-Confirm</span></span>
<span data-ttu-id="a8ecb-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ecb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ecb-124">-WhatIf</span></span>
<span data-ttu-id="a8ecb-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ecb-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8ecb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ecb-127">-DefaultProfile</span></span>
<span data-ttu-id="a8ecb-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8ecb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ecb-129">CommonParameters</span></span>
<span data-ttu-id="a8ecb-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ecb-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ecb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ecb-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8ecb-132">INPUTS</span></span>

## <span data-ttu-id="a8ecb-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8ecb-133">OUTPUTS</span></span>

### <span data-ttu-id="a8ecb-134">logiczną</span><span class="sxs-lookup"><span data-stu-id="a8ecb-134">bool</span></span>
<span data-ttu-id="a8ecb-135">Jeśli PassThru jest określony, zwraca wartość Prawda po wykonaniu operacji.</span><span class="sxs-lookup"><span data-stu-id="a8ecb-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="a8ecb-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8ecb-136">NOTES</span></span>

## <span data-ttu-id="a8ecb-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8ecb-137">RELATED LINKS</span></span>

[<span data-ttu-id="a8ecb-138">Nowe — AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="a8ecb-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="a8ecb-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="a8ecb-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


