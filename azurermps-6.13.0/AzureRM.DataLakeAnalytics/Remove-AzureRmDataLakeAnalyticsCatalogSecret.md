---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: aa7dace3141210e8c4ff6055a011f34523c5b586
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541755"
---
# <span data-ttu-id="e374d-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e374d-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="e374d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e374d-102">SYNOPSIS</span></span>
<span data-ttu-id="e374d-103">Usuwa klucz tajny Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e374d-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e374d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e374d-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e374d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e374d-105">DESCRIPTION</span></span>
<span data-ttu-id="e374d-106">Polecenie cmdlet **Remove-AzureRmDataLakeAnalyticsCatalogSecret** usuwa hasło wykazu usługi Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e374d-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="e374d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e374d-107">EXAMPLES</span></span>

### <span data-ttu-id="e374d-108">Przykład 1. Usuń klucz tajny</span><span class="sxs-lookup"><span data-stu-id="e374d-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="e374d-109">To polecenie usuwa określone hasło wykazu usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e374d-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="e374d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e374d-110">PARAMETERS</span></span>

### <span data-ttu-id="e374d-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="e374d-111">-Account</span></span>
<span data-ttu-id="e374d-112">Określa nazwę konta usługi Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e374d-112">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e374d-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e374d-113">-DatabaseName</span></span>
<span data-ttu-id="e374d-114">Określa nazwę bazy danych, która zawiera klucz tajny.</span><span class="sxs-lookup"><span data-stu-id="e374d-114">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="e374d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e374d-115">-DefaultProfile</span></span>
<span data-ttu-id="e374d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e374d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e374d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e374d-117">-Force</span></span>
<span data-ttu-id="e374d-118">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e374d-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e374d-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e374d-119">-Name</span></span>
<span data-ttu-id="e374d-120">Określa nazwę wpisu tajnego.</span><span class="sxs-lookup"><span data-stu-id="e374d-120">Specifies the name of the secret.</span></span>

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

### <span data-ttu-id="e374d-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e374d-121">-PassThru</span></span>
<span data-ttu-id="e374d-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e374d-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e374d-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e374d-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e374d-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e374d-124">-Confirm</span></span>
<span data-ttu-id="e374d-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e374d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e374d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e374d-126">-WhatIf</span></span>
<span data-ttu-id="e374d-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e374d-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e374d-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e374d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e374d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e374d-129">CommonParameters</span></span>
<span data-ttu-id="e374d-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e374d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e374d-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e374d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e374d-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e374d-132">INPUTS</span></span>

### <span data-ttu-id="e374d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e374d-133">System.String</span></span>

## <span data-ttu-id="e374d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e374d-134">OUTPUTS</span></span>

### <span data-ttu-id="e374d-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e374d-135">System.Boolean</span></span>

## <span data-ttu-id="e374d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e374d-136">NOTES</span></span>

## <span data-ttu-id="e374d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e374d-137">RELATED LINKS</span></span>

[<span data-ttu-id="e374d-138">Nowe — AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e374d-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="e374d-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="e374d-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


