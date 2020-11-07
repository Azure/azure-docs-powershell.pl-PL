---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48D6288A-EBE1-44FD-B871-80A0681BBEA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlservercommunicationlink
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerCommunicationLink.md
ms.openlocfilehash: 3d2137aa1398e5bb3b8173b6ea927c4deb50d41f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719063"
---
# <span data-ttu-id="1e858-101">Remove-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="1e858-101">Remove-AzureRmSqlServerCommunicationLink</span></span>

## <span data-ttu-id="1e858-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e858-102">SYNOPSIS</span></span>
<span data-ttu-id="1e858-103">Umożliwia usunięcie łącza komunikacyjnego dla transakcji Elastic Database między dwoma serwerami.</span><span class="sxs-lookup"><span data-stu-id="1e858-103">Deletes a communication link for elastic database transactions between two servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e858-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e858-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerCommunicationLink [-LinkName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e858-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1e858-105">DESCRIPTION</span></span>
<span data-ttu-id="1e858-106">Polecenie cmdlet **Remove-AzureRmSqlServerCommunicationLink** usuwa link komunikacji między serwerami dla transakcji Elastic Database w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="1e858-106">The **Remove-AzureRmSqlServerCommunicationLink** cmdlet deletes a server-to-server communication link for elastic database transactions in Azure SQL Database.</span></span>

## <span data-ttu-id="1e858-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e858-107">EXAMPLES</span></span>

### <span data-ttu-id="1e858-108">Przykład 1: Usuwanie łącza komunikacyjnego</span><span class="sxs-lookup"><span data-stu-id="1e858-108">Example 1: Delete a communication link</span></span>
```
PS C:\>Remove-AzureRmSqlServerCommunicationLink -ResourceGroupName "ResourceGroup01" -ServerName "ContosoServer17" -LinkName "Link01"
```

<span data-ttu-id="1e858-109">To polecenie powoduje usunięcie linku komunikacyjnego serwer-do-serwera o nazwie Link01 na ContosoServer17.</span><span class="sxs-lookup"><span data-stu-id="1e858-109">This command deletes a server-to-server communication link named Link01 on ContosoServer17.</span></span>

## <span data-ttu-id="1e858-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e858-110">PARAMETERS</span></span>

### <span data-ttu-id="1e858-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e858-111">-DefaultProfile</span></span>
<span data-ttu-id="1e858-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1e858-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e858-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1e858-113">-Force</span></span>
<span data-ttu-id="1e858-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1e858-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e858-115">-Linkname</span><span class="sxs-lookup"><span data-stu-id="1e858-115">-LinkName</span></span>
<span data-ttu-id="1e858-116">Określa nazwę łącza komunikacyjnego serwera, które zostanie usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e858-116">Specifies the name of the server communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="1e858-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e858-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e858-118">Określa nazwę grupy zasobów, do której należy serwer określony przez parametr *nazwa_serwera* .</span><span class="sxs-lookup"><span data-stu-id="1e858-118">Specifies the name of the resource group to which the server specified by the *ServerName* parameter belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e858-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="1e858-119">-ServerName</span></span>
<span data-ttu-id="1e858-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="1e858-120">Specifies the name of a server.</span></span>
<span data-ttu-id="1e858-121">Ten serwer zawiera łącze komunikacyjne, które zostało usunięte przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e858-121">This server contains the communication link that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="1e858-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e858-122">-Confirm</span></span>
<span data-ttu-id="1e858-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e858-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e858-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e858-124">-WhatIf</span></span>
<span data-ttu-id="1e858-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e858-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e858-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1e858-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e858-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e858-127">CommonParameters</span></span>
<span data-ttu-id="1e858-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e858-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e858-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e858-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e858-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e858-130">INPUTS</span></span>

### <span data-ttu-id="1e858-131">System. String</span><span class="sxs-lookup"><span data-stu-id="1e858-131">System.String</span></span>

## <span data-ttu-id="1e858-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e858-132">OUTPUTS</span></span>

### <span data-ttu-id="1e858-133">Microsoft. Azure. Commands. SQL. ServerCommunicationLink. model. AzureSqlServerCommunicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="1e858-133">Microsoft.Azure.Commands.Sql.ServerCommunicationLink.Model.AzureSqlServerCommunicationLinkModel</span></span>

## <span data-ttu-id="1e858-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e858-134">NOTES</span></span>
* <span data-ttu-id="1e858-135">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="1e858-135">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="1e858-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e858-136">RELATED LINKS</span></span>

[<span data-ttu-id="1e858-137">Get-AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="1e858-137">Get-AzureRmSqlServerCommunicationLink</span></span>](./Get-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="1e858-138">Nowe — AzureRmSqlServerCommunicationLink</span><span class="sxs-lookup"><span data-stu-id="1e858-138">New-AzureRmSqlServerCommunicationLink</span></span>](./New-AzureRmSqlServerCommunicationLink.md)

[<span data-ttu-id="1e858-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="1e858-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
