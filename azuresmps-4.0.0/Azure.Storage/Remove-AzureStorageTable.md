---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcb08eb9e63917d072630f81a2026d961a70dd27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710678"
---
# <span data-ttu-id="833cf-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="833cf-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="833cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="833cf-102">SYNOPSIS</span></span>
<span data-ttu-id="833cf-103">Usuwa tabelę magazynu.</span><span class="sxs-lookup"><span data-stu-id="833cf-103">Removes a storage table.</span></span>

## <span data-ttu-id="833cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="833cf-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="833cf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="833cf-105">DESCRIPTION</span></span>
<span data-ttu-id="833cf-106">Polecenie cmdlet **Remove-AzureStorageTable** usuwa co najmniej jeden magazyn z konta magazynu na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="833cf-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="833cf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="833cf-107">EXAMPLES</span></span>

### <span data-ttu-id="833cf-108">Przykład 1. Usuwanie tabeli</span><span class="sxs-lookup"><span data-stu-id="833cf-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="833cf-109">To polecenie umożliwia usunięcie tabeli.</span><span class="sxs-lookup"><span data-stu-id="833cf-109">This command removes a table.</span></span>

### <span data-ttu-id="833cf-110">Przykład 2: Usuwanie kilku tabel</span><span class="sxs-lookup"><span data-stu-id="833cf-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="833cf-111">W tym przykładzie użyto symbolu wieloznacznego z parametrem *name* w celu uzyskania wszystkich tabel pasujących do tabeli wzorzec, a następnie przekazanie wyniku w potoku w celu usunięcia tabel.</span><span class="sxs-lookup"><span data-stu-id="833cf-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="833cf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="833cf-112">PARAMETERS</span></span>

### <span data-ttu-id="833cf-113">-Context</span><span class="sxs-lookup"><span data-stu-id="833cf-113">-Context</span></span>
<span data-ttu-id="833cf-114">Określa kontekst usługi Azure Storage.</span><span class="sxs-lookup"><span data-stu-id="833cf-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="833cf-115">Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="833cf-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="833cf-116">-Force</span><span class="sxs-lookup"><span data-stu-id="833cf-116">-Force</span></span>
<span data-ttu-id="833cf-117">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="833cf-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833cf-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="833cf-118">-Name</span></span>
<span data-ttu-id="833cf-119">Określa nazwę tabeli, która ma zostać usunięta.</span><span class="sxs-lookup"><span data-stu-id="833cf-119">Specifies the name of the table to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="833cf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="833cf-120">-PassThru</span></span>
<span data-ttu-id="833cf-121">Wskazuje, że to polecenie cmdlet zwraca **wartość logiczną** odzwierciedlającą sukces operacji.</span><span class="sxs-lookup"><span data-stu-id="833cf-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="833cf-122">Domyślnie to polecenie cmdlet nie zwraca wartości.</span><span class="sxs-lookup"><span data-stu-id="833cf-122">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="833cf-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="833cf-123">-Confirm</span></span>
<span data-ttu-id="833cf-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="833cf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="833cf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="833cf-125">-WhatIf</span></span>
<span data-ttu-id="833cf-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="833cf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="833cf-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="833cf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="833cf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="833cf-128">CommonParameters</span></span>
<span data-ttu-id="833cf-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="833cf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="833cf-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="833cf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="833cf-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="833cf-131">INPUTS</span></span>

## <span data-ttu-id="833cf-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="833cf-132">OUTPUTS</span></span>

## <span data-ttu-id="833cf-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="833cf-133">NOTES</span></span>

## <span data-ttu-id="833cf-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="833cf-134">RELATED LINKS</span></span>

[<span data-ttu-id="833cf-135">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="833cf-135">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
