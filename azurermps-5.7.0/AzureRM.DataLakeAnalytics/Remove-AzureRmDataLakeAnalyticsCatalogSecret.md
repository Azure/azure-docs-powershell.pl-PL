---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 2ee08eaf9dae9a6d2001608d8ef247c7e116c98e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542644"
---
# <span data-ttu-id="dcae1-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="dcae1-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="dcae1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dcae1-102">SYNOPSIS</span></span>
<span data-ttu-id="dcae1-103">Usuwa klucz tajny Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dcae1-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcae1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dcae1-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dcae1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dcae1-105">DESCRIPTION</span></span>
<span data-ttu-id="dcae1-106">Polecenie cmdlet **Remove-AzureRmDataLakeAnalyticsCatalogSecret** usuwa hasło wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dcae1-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="dcae1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dcae1-107">EXAMPLES</span></span>

### <span data-ttu-id="dcae1-108">Przykład 1. Usuń klucz tajny</span><span class="sxs-lookup"><span data-stu-id="dcae1-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="dcae1-109">To polecenie usuwa określone hasło wykazu usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dcae1-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="dcae1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dcae1-110">PARAMETERS</span></span>

### <span data-ttu-id="dcae1-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="dcae1-111">-Account</span></span>
<span data-ttu-id="dcae1-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="dcae1-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcae1-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dcae1-113">-DatabaseName</span></span>
<span data-ttu-id="dcae1-114">Określa nazwę bazy danych, która zawiera klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="dcae1-114">Specifies the name of the database that holds the secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcae1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcae1-115">-DefaultProfile</span></span>
<span data-ttu-id="dcae1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dcae1-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcae1-117">-Force</span><span class="sxs-lookup"><span data-stu-id="dcae1-117">-Force</span></span>
<span data-ttu-id="dcae1-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dcae1-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcae1-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dcae1-119">-Name</span></span>
<span data-ttu-id="dcae1-120">Określa nazwę wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="dcae1-120">Specifies the name of the secret.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcae1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcae1-121">-PassThru</span></span>
<span data-ttu-id="dcae1-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="dcae1-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dcae1-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="dcae1-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcae1-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dcae1-124">-Confirm</span></span>
<span data-ttu-id="dcae1-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcae1-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcae1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcae1-126">-WhatIf</span></span>
<span data-ttu-id="dcae1-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dcae1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcae1-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dcae1-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcae1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcae1-129">CommonParameters</span></span>
<span data-ttu-id="dcae1-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcae1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcae1-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcae1-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcae1-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcae1-132">INPUTS</span></span>

### <span data-ttu-id="dcae1-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dcae1-133">None</span></span>
<span data-ttu-id="dcae1-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="dcae1-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dcae1-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dcae1-135">OUTPUTS</span></span>

### <span data-ttu-id="dcae1-136">logiczną</span><span class="sxs-lookup"><span data-stu-id="dcae1-136">bool</span></span>
<span data-ttu-id="dcae1-137">Jeśli PassThru jest określony, zwraca wartość Prawda po wykonaniu operacji.</span><span class="sxs-lookup"><span data-stu-id="dcae1-137">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="dcae1-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dcae1-138">NOTES</span></span>

## <span data-ttu-id="dcae1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcae1-139">RELATED LINKS</span></span>

[<span data-ttu-id="dcae1-140">Nowe — AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="dcae1-140">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="dcae1-141">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="dcae1-141">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


