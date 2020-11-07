---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 47b14128d707d4a0c06577f4b677627e6933fa29
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705766"
---
# <span data-ttu-id="fc0eb-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="fc0eb-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="fc0eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc0eb-102">SYNOPSIS</span></span>
<span data-ttu-id="fc0eb-103">Modyfikuje liczbę ósemkową uprawnień pliku lub folderu w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fc0eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc0eb-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc0eb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fc0eb-105">DESCRIPTION</span></span>
<span data-ttu-id="fc0eb-106">Polecenie cmdlet **Set-AzDataLakeStoreItemPermission** modyfikuje liczbę ósemkową określoną przez plik lub folder w usłudze Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fc0eb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc0eb-107">EXAMPLES</span></span>

### <span data-ttu-id="fc0eb-108">Przykład 1: Ustawianie liczby ósemkowej uprawnień dla elementu</span><span class="sxs-lookup"><span data-stu-id="fc0eb-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="fc0eb-109">To polecenie umożliwia ustawienie liczby ósemkowej uprawnień dla pliku na 0770, co tłumaczy, aby wyczyścić bit, ustawić uprawnienia do odczytu/zapisu/wykonywania dla właściciela pliku, ustawić uprawnienia do odczytu/zapisu/wykonywania dla grupy plików, a następnie wyczyścić uprawnienia do odczytu/zapisu/wykonywania.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="fc0eb-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc0eb-110">PARAMETERS</span></span>

### <span data-ttu-id="fc0eb-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="fc0eb-111">-Account</span></span>
<span data-ttu-id="fc0eb-112">Określa nazwę konta usługi Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="fc0eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc0eb-113">-DefaultProfile</span></span>
<span data-ttu-id="fc0eb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc0eb-115">-Path</span><span class="sxs-lookup"><span data-stu-id="fc0eb-115">-Path</span></span>
<span data-ttu-id="fc0eb-116">Określa ścieżkę pliku lub folderu w usłudze Data Lake Store, rozpoczynając od katalogu głównego (/).</span><span class="sxs-lookup"><span data-stu-id="fc0eb-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0eb-117">-Uprawnienie</span><span class="sxs-lookup"><span data-stu-id="fc0eb-117">-Permission</span></span>
<span data-ttu-id="fc0eb-118">Uprawnienia do ustawiania pliku lub folderu wyrażone jako ósemkowa (na przykład ' 777 ')</span><span class="sxs-lookup"><span data-stu-id="fc0eb-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc0eb-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc0eb-119">-Confirm</span></span>
<span data-ttu-id="fc0eb-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc0eb-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc0eb-121">-WhatIf</span></span>
<span data-ttu-id="fc0eb-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc0eb-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc0eb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc0eb-124">CommonParameters</span></span>
<span data-ttu-id="fc0eb-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc0eb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc0eb-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc0eb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc0eb-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc0eb-127">INPUTS</span></span>

### <span data-ttu-id="fc0eb-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fc0eb-128">System.String</span></span>

### <span data-ttu-id="fc0eb-129">Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fc0eb-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="fc0eb-130">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fc0eb-130">System.Int32</span></span>

## <span data-ttu-id="fc0eb-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc0eb-131">OUTPUTS</span></span>

### <span data-ttu-id="fc0eb-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc0eb-132">System.Boolean</span></span>

## <span data-ttu-id="fc0eb-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc0eb-133">NOTES</span></span>
* <span data-ttu-id="fc0eb-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="fc0eb-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="fc0eb-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc0eb-135">RELATED LINKS</span></span>

[<span data-ttu-id="fc0eb-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="fc0eb-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)

