---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 03e43530a044bad5f3ea7509fa649da9f26a93f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524454"
---
# <span data-ttu-id="c7fbc-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbc-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="c7fbc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="c7fbc-103">Usuwa plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7fbc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7fbc-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7fbc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c7fbc-105">DESCRIPTION</span></span>
<span data-ttu-id="c7fbc-106">Polecenie cmdlet **Remove-AzureRmDataLakeStoreItem** usuwa plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c7fbc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7fbc-107">EXAMPLES</span></span>

### <span data-ttu-id="c7fbc-108">Przykład 1: usuwanie wielu elementów</span><span class="sxs-lookup"><span data-stu-id="c7fbc-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="c7fbc-109">To polecenie usuwa pliki File01.txt i File.csv z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="c7fbc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7fbc-110">PARAMETERS</span></span>

### <span data-ttu-id="c7fbc-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="c7fbc-111">-Account</span></span>
<span data-ttu-id="c7fbc-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c7fbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7fbc-113">-DefaultProfile</span></span>
<span data-ttu-id="c7fbc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7fbc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c7fbc-115">-Force</span></span>
<span data-ttu-id="c7fbc-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7fbc-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7fbc-117">-PassThru</span></span>
<span data-ttu-id="c7fbc-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c7fbc-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7fbc-120">-Ścieżki</span><span class="sxs-lookup"><span data-stu-id="c7fbc-120">-Paths</span></span>
<span data-ttu-id="c7fbc-121">Określa tablicę ścieżek plików do usunięcia, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="c7fbc-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7fbc-122">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="c7fbc-122">-Recurse</span></span>
<span data-ttu-id="c7fbc-123">Wskazuje, że ta operacja powoduje usunięcie wszystkich elementów w folderze docelowym, łącznie z podfolderami.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7fbc-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c7fbc-124">-Confirm</span></span>
<span data-ttu-id="c7fbc-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7fbc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7fbc-126">-WhatIf</span></span>
<span data-ttu-id="c7fbc-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7fbc-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7fbc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7fbc-129">CommonParameters</span></span>
<span data-ttu-id="c7fbc-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7fbc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7fbc-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7fbc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7fbc-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7fbc-132">INPUTS</span></span>

### <span data-ttu-id="c7fbc-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c7fbc-133">System.String</span></span>

### <span data-ttu-id="c7fbc-134">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="c7fbc-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="c7fbc-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c7fbc-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c7fbc-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7fbc-136">OUTPUTS</span></span>

### <span data-ttu-id="c7fbc-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7fbc-137">System.Boolean</span></span>

## <span data-ttu-id="c7fbc-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7fbc-138">NOTES</span></span>

## <span data-ttu-id="c7fbc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7fbc-139">RELATED LINKS</span></span>

[<span data-ttu-id="c7fbc-140">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbc-140">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c7fbc-141">Eksportowanie — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbc-141">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c7fbc-142">Import — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbc-142">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c7fbc-143">Dołącz do AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbc-143">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c7fbc-144">Nowe — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbc-144">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c7fbc-145">Test — AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c7fbc-145">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


