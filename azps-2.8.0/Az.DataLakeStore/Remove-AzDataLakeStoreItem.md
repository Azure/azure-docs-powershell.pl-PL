---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 1ad6fbd77bc827b1cccd3074198182489186d06b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705789"
---
# <span data-ttu-id="0dd4e-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0dd4e-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="0dd4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0dd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd4e-103">Usuwa plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0dd4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0dd4e-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0dd4e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0dd4e-105">DESCRIPTION</span></span>
<span data-ttu-id="0dd4e-106">Polecenie cmdlet **Remove-AzDataLakeStoreItem** usuwa plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0dd4e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0dd4e-107">EXAMPLES</span></span>

### <span data-ttu-id="0dd4e-108">Przykład 1: usuwanie wielu elementów</span><span class="sxs-lookup"><span data-stu-id="0dd4e-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="0dd4e-109">To polecenie usuwa pliki File01.txt i File.csv z usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="0dd4e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0dd4e-110">PARAMETERS</span></span>

### <span data-ttu-id="0dd4e-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="0dd4e-111">-Account</span></span>
<span data-ttu-id="0dd4e-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0dd4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd4e-113">-DefaultProfile</span></span>
<span data-ttu-id="0dd4e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dd4e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0dd4e-115">-Force</span></span>
<span data-ttu-id="0dd4e-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0dd4e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0dd4e-117">-PassThru</span></span>
<span data-ttu-id="0dd4e-118">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0dd4e-119">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0dd4e-120">-Ścieżki</span><span class="sxs-lookup"><span data-stu-id="0dd4e-120">-Paths</span></span>
<span data-ttu-id="0dd4e-121">Określa tablicę ścieżek plików do usunięcia, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="0dd4e-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0dd4e-122">-Rekursywowanie</span><span class="sxs-lookup"><span data-stu-id="0dd4e-122">-Recurse</span></span>
<span data-ttu-id="0dd4e-123">Wskazuje, że ta operacja powoduje usunięcie wszystkich elementów w folderze docelowym, łącznie z podfolderami.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="0dd4e-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0dd4e-124">-Confirm</span></span>
<span data-ttu-id="0dd4e-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0dd4e-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0dd4e-126">-WhatIf</span></span>
<span data-ttu-id="0dd4e-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0dd4e-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0dd4e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd4e-129">CommonParameters</span></span>
<span data-ttu-id="0dd4e-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dd4e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd4e-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dd4e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd4e-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dd4e-132">INPUTS</span></span>

### <span data-ttu-id="0dd4e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0dd4e-133">System.String</span></span>

### <span data-ttu-id="0dd4e-134">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="0dd4e-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="0dd4e-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0dd4e-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0dd4e-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0dd4e-136">OUTPUTS</span></span>

### <span data-ttu-id="0dd4e-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0dd4e-137">System.Boolean</span></span>

## <span data-ttu-id="0dd4e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0dd4e-138">NOTES</span></span>

## <span data-ttu-id="0dd4e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0dd4e-139">RELATED LINKS</span></span>

[<span data-ttu-id="0dd4e-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0dd4e-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="0dd4e-141">Eksportowanie — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0dd4e-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="0dd4e-142">Import — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0dd4e-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="0dd4e-143">Dołącz do AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0dd4e-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="0dd4e-144">Nowe — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0dd4e-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="0dd4e-145">Test — AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0dd4e-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


